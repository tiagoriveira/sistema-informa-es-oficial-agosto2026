# ARQUITETURA

Documento de projeto do STUDY-BRAIN. Descreve **o sistema que existe de fato**, as mudanças em
relação ao briefing original e o que ficou de fora.

Ordem de prioridade que guiou todas as decisões abaixo:
**simplicidade → confiabilidade → qualidade do contexto da IA → manutenção → escalabilidade.**

---

## 1. Arquitetura final

```
Sistema-de-estudos-tiago-agosto-2026/
│
├── CLAUDE.md                  ← constituição. Carregada automaticamente pelo Claude Code
├── INICIO.md                  ← estado atual + porta de entrada (humano e IA)
│
├── RAW/                       ← fontes originais. Imutável. Só o Tiago escreve
│   └── <disciplina>/
│
├── KNOWLEDGE/                 ← conhecimento sobre o assunto (3 níveis, ver #8)
│   └── <hub>/<disciplina>/
│       ├── mapa-<disciplina>.md
│       ├── fase-N-<slug>/<conceito>.md
│       └── fontes/<fonte>.md
│
├── LEARNER/                   ← modelo do aluno
│   ├── perfil.md
│   └── estado-<disciplina>.md
│
├── SESSIONS/                  ← AAAA-MM-DD-<disciplina>.md — arquivo, não memória de trabalho
│
├── INBOX/                     ← notas pessoais cruas, sem categoria (desde 2026-08-15)
│                                 não entra na leitura automática — só lido sob pedido de triagem
│
├── SYSTEM/
│   ├── schema.md              ← formatos de página (leitura sob demanda)
│   ├── index.md               ← catálogo com resumo de uma linha por página
│   ├── log.md                 ← linha do tempo append-only
│   ├── ARQUITETURA.md         ← este arquivo
│   └── FAQ.md
│
└── _templates/                ← 5 templates
```

### Fluxo de retomada ("continue de onde paramos")

```
pedido do Tiago
   ↓
INICIO.md ................. disciplina ativa, revisões vencidas, próxima ação   [1 arquivo]
   ↓
LEARNER/estado-<disc>.md .. estado de cada conceito, evidências, confusões      [1 arquivo]
   ↓
decisão pedagógica ........ revisar / corrigir / testar lacuna / avançar
   ↓
KNOWLEDGE/<1-3 páginas> ... só o conteúdo do que vai ser trabalhado agora
   ↓
pergunta (active recall)
   ↓
veredito → escreve LEARNER imediatamente
   ↓
fim da sessão → SESSIONS/ + revisões recalculadas + INICIO.md + log.md
```

Custo de retomada: **2 arquivos pequenos**, constante ao longo dos anos. Esta é a propriedade
central do desenho — sem ela o sistema morre por peso próprio no segundo ano.

### Onde mora a verdade

| Sobre | Fonte da verdade | Derivado (reconstruível) |
|---|---|---|
| as fontes | `RAW/` | — |
| o assunto | `KNOWLEDGE/` | reconstruível a partir de RAW |
| o aluno | `LEARNER/` | reconstruível a partir de SESSIONS |
| o que aconteceu | `SESSIONS/` + `log.md` | — |
| pensamento cru do Tiago | `INBOX/` | — (não é fonte, não é KNOWLEDGE) |
| navegação | — | `INICIO.md`, `index.md` (100% derivados) |

Regra de conflito: **LEARNER vence INICIO.md**. `INICIO.md` e `index.md` são caches; se
estiverem errados, são regenerados, nunca defendidos.

### Ferramentas

| Componente | Decisão | Motivo |
|---|---|---|
| Obsidian Core | **sim** | leitura, links, graph view. Zero configuração |
| Claude Code Desktop | **sim** | é a IA com acesso direto ao vault; `CLAUDE.md` é auto-carregado |
| `grep` / ripgrep | **sim** | já existe, resolve toda a busca nesta escala |
| Git | **opcional** | recomendado; instruções no FAQ. Não iniciado sem seu pedido |
| Obsidian Web Clipper | **opcional** | só se você for capturar artigos web |
| Dataview | **não** | ver mudança #12 |
| Embeddings / BM25 / vector DB | **não** | ver mudança #13 |
| MCP / API / scripts / automações | **não** | ver mudança #13 |

---

## 2. Mudanças em relação ao briefing original

Cada mudança: o que mudou, por quê, que problema resolve, benefício, trade-off.

---

### #1 — LEARNER: de 4 arquivos por disciplina para 1

**Briefing:** `LEARNER/Economia/{dominio,lacunas,erros,revisoes}.md` — e a seção 6 lista 7
dimensões (domínio, lacunas, erros, confusões, confiança, revisão, histórico), o que levaria
a 7 arquivos por disciplina.

**Agora:** `LEARNER/estado-<disciplina>.md`, um bloco por conceito, todas as dimensões juntas.

**Por quê:** as 7 dimensões não são 7 assuntos — são 7 atributos do **mesmo** conceito.
"Elasticidade" apareceria em `lacunas.md`, `erros.md` e `revisoes.md` ao mesmo tempo.

**Problema que resolve:** amplificação de escrita e divergência garantida. Um único veredito
("errou elasticidade") exigiria 3 a 4 edições coordenadas. Toda vez que uma delas falhasse —
e falharia — os arquivos se contradiriam, e não haveria como saber qual está certo. Um modelo
do aluno que se contradiz é pior que nenhum: a IA toma decisão pedagógica com dado errado.
Havia ainda uma colisão de nomes: `[[dominio]]` seria ambíguo entre disciplinas no Obsidian.

**Benefícios:** atualização atômica (um conceito = uma edição em um lugar); a IA lê um arquivo
e vê tudo sobre o aluno naquela disciplina; impossível divergir de si mesmo.

**Trade-off:** o arquivo cresce. Mitigado por: máximo 5 evidências por conceito, e regra de
dividir por tema acima de ~300 linhas. Também se perde a visão "todos os meus erros de uma vez"
em um arquivo só — recuperável com `grep -n "errou" LEARNER/estado-economia.md`.

---

### #2 — `INICIO.md`: cache de retomada (novo)

**Briefing:** o fluxo de retomada era `INDEX → KNOWLEDGE → LEARNER → sessões anteriores`.

**Agora:** `INICIO.md` na raiz — disciplina ativa, última sessão, revisões vencidas, próxima
ação recomendada. Reescrito ao fim de toda sessão.

**Por quê:** o fluxo do briefing gasta 4+ leituras antes de qualquer ato pedagógico, e o
`index.md` (catálogo de conteúdo) não é o arquivo certo para responder "onde eu parei?" —
ele descreve o que existe, não o que está pendente.

**Problema que resolve:** custo e latência da retomada, e o risco de a IA "quase" reconstruir
o estado a partir de fontes espalhadas e errar a decisão inicial da sessão.

**Benefícios:** "continue" vira uma leitura. É também o painel humano — você abre o vault no
Obsidian e vê onde está, sem perguntar nada à IA.

**Trade-off:** é dado duplicado, logo pode ficar obsoleto. Aceito porque é explicitamente
declarado **derivado**: em conflito, LEARNER vence, e o LINT o regenera. Um cache que se sabe
cache é seguro; um cache que se acha fonte da verdade é bug.

---

### #3 — Constituição em `CLAUDE.md`, formatos em `schema.md`

**Briefing:** `SYSTEM/schema.md` como "constituição do sistema".

**Agora:** `CLAUDE.md` na raiz é a constituição (regras sempre ativas, curto).
`SYSTEM/schema.md` é a referência de formato de página (longo, lido sob demanda).

**Por quê:** um detalhe operacional decisivo — o Claude Code carrega o `CLAUDE.md` da raiz
automaticamente, em toda sessão. Um `SYSTEM/schema.md` só é lido se alguém lembrar de pedir.
A constituição precisa estar onde ela é lida sem depender de disciplina do usuário.

**Problema que resolve:** o risco de a IA operar sem as regras — que é o modo de falha mais
grave possível aqui, e o mais silencioso, porque a resposta continua parecendo boa.

**Benefícios:** regras sempre carregadas; constituição curta e legível; formato longo não
ocupa contexto quando não é necessário. Dois arquivos, dois papéis, sem sobreposição.

**Trade-off:** dois lugares para consultar em vez de um. Mitigado por uma fronteira clara:
`CLAUDE.md` nunca traz formato, `schema.md` nunca traz regra de comportamento.

---

### #4 — Memória escrita durante a sessão, não no fim

**Briefing:** a sessão atualiza a memória; implicitamente, ao final.

**Agora:** o bloco do conceito no LEARNER é atualizado **logo após cada veredito**. Só a nota
de sessão, as datas de revisão e o `INICIO.md` são escritos no fechamento. Se 3+ conceitos
foram avaliados e nada foi escrito, a IA grava um checkpoint sem esperar pedido.

**Por quê:** sessão de estudo não termina de forma limpa. Termina quando toca o telefone.

**Problema que resolve:** perda total do aprendizado da sessão se a janela for fechada sem
"fechar a sessão" — que é o caso comum, não a exceção.

**Benefícios:** o pior caso passa de "perdi tudo" para "perdi a narrativa da sessão, mas o
estado dos conceitos está salvo". Durabilidade sem exigir ritual do usuário.

**Trade-off:** mais escritas pequenas ao longo da conversa, e um diff de Git mais fragmentado.
Barato perto do que evita.

---

### #5 — Orçamento de leitura explícito; `SESSIONS/` nunca é relido

**Briefing:** o fluxo inclui "sessões anteriores" como etapa de consulta.

**Agora:** regra dura — a IA lê `INICIO.md` + `LEARNER/`, e no máximo a **última** sessão se
faltar contexto. Nunca o histórico. Se algo relevante só existe numa sessão antiga, isso é
tratado como defeito a ser destilado para o LEARNER.

**Por quê:** o número de sessões cresce sem limite; o modelo do aluno, não. Ler sessões é
re-derivar conhecimento que já foi compilado — exatamente o que o LLM Wiki existe para evitar.

**Problema que resolve:** degradação inevitável no ano 2. Com 200 sessões, "continue" ou fica
caro, ou lê uma amostra arbitrária e decide com base incompleta.

**Benefícios:** custo constante; e um efeito de qualidade — obriga a IA a manter o LEARNER
realmente completo, porque é a única memória que ela vai reler.

**Trade-off:** o que não for destilado na hora está efetivamente esquecido para fins de
tutoria (embora preservado para auditoria). É o preço de ter memória de trabalho limitada, e
é o mesmo compromisso que a memória humana faz.

---

### #6 — Estados com critério observável, e `nivel` separado do estado

**Briefing:** proíbe tratar porcentagens como medição científica, mas ainda admite "níveis"
como indicadores internos aproximados.

**Agora:** vocabulário fechado de 4 estados, cada um com **critério comportamental
verificável** (ex.: `consolidado` = explicou certo, sem ajuda, em 2+ ocasiões em dias
diferentes, incluindo uma recuperação após 7+ dias). E `nivel` (1–5) existe só como contador
de agendamento da escada de revisão, declarado explicitamente como **não** sendo medida de
conhecimento. Nenhum número no frontmatter.

**Por quê:** "indicador aproximado" degenera. Um LLM que pode escrever `confiança: 0.7` vai
escrever, e o número parece dado quando é palpite — e na sessão seguinte ele é lido como fato.

**Problema que resolve:** métrica inventada que se auto-confirma. Também resolve a
inconsistência entre sessões: sem critério explícito, o mesmo desempenho vira "médio" hoje e
"bom" amanhã.

**Benefícios:** todo estado é auditável — você pode discordar apontando a evidência. Força a
IA a registrar o que **aconteceu** em vez de o que ela **acha**. Separar agendamento de
avaliação deixa as duas coisas honestas.

**Trade-off:** granularidade menor. Não dá para desenhar gráfico de progresso a partir disso,
e a diferença entre "quase consolidado" e "em desenvolvimento" some. Decisão consciente: um
gráfico bonito de dado inventado é pior que nenhum gráfico.

---

### #7 — `RAW/` por disciplina, não por tipo de mídia

**Briefing:** `RAW/{livros,artigos,PDFs,cursos,aulas,outros}/`.

**Agora:** `RAW/<disciplina>/`. O tipo de mídia é metadado da página de fonte.

**Por quê:** ninguém procura "um PDF qualquer". Procura-se por assunto. Além disso, as
categorias do briefing se sobrepõem — um PDF de um livro de um curso cabe em três pastas, e
esse tipo de ambiguidade termina em `outros/` com metade do acervo dentro.

**Problema que resolve:** decisão de arquivamento ambígua, e o fato de que INGEST é sempre
uma operação com escopo de disciplina.

**Benefícios:** um lugar óbvio para cada arquivo; o escopo de disciplina fica visível no
sistema de arquivos.

**Trade-off:** fonte interdisciplinar precisa de um lar principal. Convenção: disciplina
principal, referência cruzada na página de fonte.

---

### #8 — KNOWLEDGE em 3 níveis: hub → disciplina → fase

**Briefing:** `KNOWLEDGE/{conceitos,temas,fontes}/` no topo.

**Versão de 2026-08-12 (superada):** `KNOWLEDGE/<disciplina>/` plano, conceitos na raiz, tema
como seção do mapa. A razão era que reordenar tema custava mover uma linha, não um arquivo.

**Agora (2026-08-14):** três níveis — `KNOWLEDGE/<hub>/<disciplina>/fase-N-<slug>/`, com
`mapa-<disciplina>.md` sozinho no nível da disciplina e `fontes/` como irmã das fases.
Formato completo em [[schema]] §0.

**Por quê mudou:** quando a decisão original foi tomada não existia grade curricular. Hoje
cada disciplina tem uma grade estável em fases ([[schema]] §3), e a fase é uma divisão real e
duradoura — não um agrupamento improvisado. Com isso o argumento "mover linha é mais barato
que mover arquivo" perde força: fase quase não muda. Os hubs vieram do mesmo pedido —
agrupar disciplinas irmãs (`filosofia/` conterá história, epistemologia, lógica, ética).

**Problema que resolve:** a pasta plana não mostrava progressão. Abrir `KNOWLEDGE/filosofia/`
dava 9 arquivos em ordem alfabética, sem dizer o que vem antes do quê — a informação só
existia no mapa. Agora a árvore de arquivos e a grade contam a mesma história.

**Benefícios:** navegação por sistema de arquivos passa a funcionar; escopo de fase visível;
espaço para a disciplina crescer dentro do hub sem virar pasta de 200 arquivos.

**Trade-off:** conceito que muda de fase agora é mover arquivo, não editar linha. E conceito
que pertence a duas fases não tem lar óbvio — a convenção é deixar na fase onde é ensinado
primeiro e linkar da outra. Os `[[links]]` **não** quebram com a mudança (invariante 6: o
Obsidian resolve por nome de arquivo, não por caminho), o que tornou a migração segura.

---

### #9 — Nomes únicos no vault + regra de desambiguação

**Briefing:** usa `[[Elasticidade]]`, `dominio.md` por disciplina.

**Agora:** todo nome de arquivo é único no vault inteiro, em kebab-case; colisão resolve com
sufixo de disciplina (`elasticidade-economia.md`). Arquivos de estado são `estado-<disciplina>.md`.

**Por quê:** o wikilink do Obsidian resolve por **nome de arquivo**, não por caminho. Dois
`dominio.md` tornam `[[dominio]]` ambíguo e o link vai para o arquivo errado silenciosamente.

**Problema que resolve:** links que apontam para o lugar errado sem erro visível — o pior tipo
de defeito, porque a IA lê o arquivo errado e responde com confiança.

**Benefícios:** links confiáveis; graph view correta; `grep` por nome sempre encontra um alvo.

**Trade-off:** nomes um pouco mais longos, e o custo de renomear se uma segunda disciplina
reivindicar o mesmo termo depois.

---

### #10 — Nota de sessão enxuta, com diagnóstico em vez de transcript

**Briefing:** 13 campos por sessão, incluindo "perguntas realizadas" e "respostas relevantes".

**Agora:** 6 seções, e a regra de registrar o **diagnóstico do erro**, não o diálogo.
"Tratou preço alto como sinal de inelasticidade" em vez de "errou a pergunta 2".

**Por quê:** registro caro demais não é preenchido, ou é preenchido com enchimento. E o
transcript já existe no histórico do chat — copiá-lo para o vault não cria memória, cria peso.

**Problema que resolve:** notas de sessão longas que ninguém lê e que a IA não pode usar,
porque a informação útil está diluída.

**Benefícios:** o que fica registrado é justamente o que muda a próxima decisão pedagógica.
O diagnóstico é reutilizável ("ele confunde causa com correlação de preço") de um jeito que
a transcrição nunca é.

**Trade-off:** perde-se a redação literal das respostas. Se você quiser reler exatamente o que
disse, é preciso o histórico do chat.

---

### #11 — Aprovação assimétrica: KNOWLEDGE pede, memória não

**Briefing:** não separa; sugere automação em ambos.

**Agora:** página nova em `KNOWLEDGE/` exige sua aprovação explícita. Atualizações de
`LEARNER/`, `SESSIONS/`, `log.md` e `INICIO.md` são automáticas.

**Por quê:** os dois têm perfis de risco opostos. Página ruim em KNOWLEDGE polui o vault
permanentemente e é você quem sabe se o conceito merece existir. Já pedir permissão para
registrar "errou elasticidade" quebra o fluxo da sessão a cada 3 minutos — e o custo de um
registro errado é baixo, porque é corrigível em uma frase.

**Problema que resolve:** os dois modos de falha extremos — vault poluído por criação
automática, e memória vazia por atrito de aprovação.

**Benefícios:** você controla o que é permanente; a IA cuida do que é volátil. Alinhado com a
convenção que você já usa no `vault-conhecimento-ia`.

**Trade-off:** o LEARNER pode acumular registro impreciso sem você perceber. Mitigado por
revisão periódica no LINT e pela facilidade de correção.

---

### #12 — Dataview: não

**Briefing:** pede avaliação; o LLM Wiki cita como possibilidade.

**Agora:** não usar.

**Por quê:** o argumento decisivo é que **a IA não lê o resultado de uma query Dataview** —
ela lê o código da query. Uma tabela de revisões pendentes gerada por Dataview é invisível
para o tutor, que é justamente quem precisa dela. Ficaria uma visão só para o humano, exigindo
disciplina de frontmatter em todo arquivo para se manter.

**Problema que resolve:** manutenção sem contrapartida, e o pior — dois caminhos divergentes
para a mesma pergunta ("o que revisar hoje?"), um para você e outro para a IA.

**Benefícios:** um caminho só, o mesmo para os dois: `grep -rn "revisar:" LEARNER/`, ou
simplesmente abrir o `INICIO.md`. Zero plugin, zero acoplamento.

**Trade-off:** sem tabelas dinâmicas no Obsidian. Se um dia você quiser um painel visual,
Dataview volta à mesa — o dado necessário já está estruturado; o custo é retroativo apenas
em mover `estado`/`revisar` para o frontmatter, e aí o granular por conceito exigiria uma
página por conceito no LEARNER, que é a mudança #1 ao contrário. Por isso: só se o ganho
visual justificar de verdade.

---

### #13 — Sem embeddings, sem banco, sem MCP, sem scripts

**Briefing:** prevê como fase posterior. Confirmado: fase posterior, não agora.

**Por quê:** nesta escala (dezenas a poucas centenas de páginas), `index.md` + links + `grep`
encontram tudo. Busca semântica resolve o problema de "não sei o nome do que procuro" — que
quase não existe aqui, porque quem nomeou as páginas foi o próprio sistema, com convenção fixa.

**Problema que resolve:** infraestrutura que precisa ser instalada, reindexada, versionada e
consertada — em um sistema cujo valor depende de ser usado todo dia sem fricção.

**Benefícios:** o vault é uma pasta de arquivos `.md`. Funciona sem instalar nada, abre em
qualquer editor, sobrevive à troca de ferramenta, faz backup com copiar e colar.

**Trade-off:** acima de ~300–500 páginas o `index.md` começa a pesar no contexto. Gatilho
objetivo para reavaliar em "Melhorias futuras".

---

### Mudanças menores

| # | Mudança | Motivo |
|---|---|---|
| 14 | `index.md` não lista sessões | seriam centenas de linhas sem resumo útil; cronologia é papel do `log.md` |
| 15 | Máx. 5 evidências por conceito no LEARNER | mantém o arquivo legível; histórico completo em SESSIONS |
| 16 | Fonte grande é ingerida por capítulo | resumo de 400 páginas numa passada sai raso demais para ensinar |
| 17 | Conceito recém-ingerido entra como `nao_iniciado` | ler sobre não é saber; evita domínio fantasma |
| 18 | `log.md` rotaciona por ano | append-only sem limite acaba grande demais para abrir |
| 19 | Página de fonte tem `## Não coberto por esta fonte` | lacuna honesta: saber o que a fonte não diz |
| 20 | Proibição de elogio automático (`CLAUDE.md` §8) | "quase isso!" em resposta errada corrompe o modelo e o aprendizado |
| 21 | Git ativo desde 2026-08-13 | remoto: `github.com/tiagoriveira/sistema-informa-es-oficial-agosto2026`; commit + push automáticos ao fim da sessão desde 2026-08-14 (comando manual no FAQ, se preferir) |
| 22 | Cinco templates em `_templates/` | funcionam com o plugin Templater, ou como copiar e colar |

---

## 3. Riscos e lacunas identificados no briefing

Levantados na análise inicial; onde foram tratados:

| Risco | Tratamento |
|---|---|
| Modelo do aluno se contradiz entre arquivos | mudança #1 |
| Custo de retomada cresce com o histórico | mudanças #2 e #5 |
| A IA opera sem ter lido as regras | mudança #3 |
| Sessão interrompida perde tudo | mudança #4 |
| Métrica inventada vira fato na sessão seguinte | mudança #6 |
| Wikilink ambíguo aponta para arquivo errado | mudança #9 |
| Vault poluído por criação automática de páginas | mudanças #11 e `CLAUDE.md` §7 |
| Conhecimento genérico da IA se disfarçando de fonte | `CLAUDE.md` §6, seção rotulada obrigatória |
| Sistema abandonado por atrito de manutenção | #10, #11, #13 — nada a instalar, nada a manter |
| Domínio fantasma (marcar como sabido o que só foi lido) | #17 e critérios de estado em #6 |

---

## 4. Limitações conhecidas

1. **A IA depende de você para saber que errou.** Se você diz "entendi" sem ter entendido, o
   modelo registra domínio que não existe. O sistema mede desempenho observável em conversa,
   não compreensão real. Perguntas de aplicação reduzem isso, não eliminam.
2. **Não existe verificação automática do vault.** Nenhum script valida links, datas ou
   formato. O LINT é a IA relendo — sujeito a erro e a esquecimento se você nunca pedir.
3. **A IA pode não seguir as regras.** `CLAUDE.md` é instrução, não garantia de execução.
   Sessão muito longa aumenta a chance de a regra escapar. Mitigação prática: sessões curtas
   e o hábito de conferir o que foi escrito.
4. **Repetição espaçada depende de você aparecer.** Nada notifica. A data de revisão só é vista
   quando você abre o vault ou pergunta.
5. **A escada de intervalos é arbitrária.** 1/3/7/16/35 é inspirada em Leitner, não calibrada
   para você nem para a dificuldade de cada conceito.
6. **PDF escaneado sem OCR não é legível.** Nem vídeo ou áudio sem transcrição.
7. **Sem acesso pelo celular.** O sistema exige o Claude Code Desktop com acesso ao disco.
   O vault sincroniza pelo OneDrive e pode ser **lido** no celular pelo Obsidian; estudar, não.
8. **Uma sessão por vez.** Duas sessões simultâneas editando o mesmo LEARNER se sobrescrevem.
   Não há travamento.
9. **`index.md` e `INICIO.md` podem envelhecer.** São derivados e regeneráveis, mas entre a
   divergência e o próximo LINT a IA pode se orientar por dado velho.
10. **Escala testada: zero.** O sistema está sendo entregue vazio. As escolhas de projeto são
    fundamentadas, não validadas por uso. Espere ajustar convenções depois das 10 primeiras
    sessões — e isso é o funcionamento correto, não falha.

---

## 5. Melhorias futuras prioritárias

Em ordem. Cada uma tem um **gatilho** — implemente quando o gatilho ocorrer, não antes.

**1. Git com commit ao fim de cada sessão.**
Gatilho: assim que você quiser. É a única melhoria que eu faria já.
Ganho: histórico completo, desfazer de qualquer corrupção, e `git log` como registro
independente do `log.md`. Custo: um comando por sessão. Comando no FAQ.

**2. Script de lint (validação mecânica).**
Gatilho: primeira vez que um LINT da IA deixar passar um link quebrado que você notou depois.
Ganho: links quebrados, datas malformadas, órfãos e conceitos fora do LEARNER viram
verificação determinística, e a IA fica com o julgamento (contradições, duplicatas
semânticas), que é onde ela é boa. ~100 linhas de Node ou Python.

**3. Dividir o LEARNER por tema.**
Gatilho: `estado-<disciplina>.md` passa de ~300 linhas.
Ganho: mantém a leitura de retomada barata. Já previsto no schema.

**4. Vista de agenda de revisões.**
Gatilho: mais de ~30 conceitos com data agendada, e você começa a perder revisões.
Ganho: uma pergunta ("o que vence esta semana?") vira resposta imediata. Faça primeiro com
`grep`; só considere Dataview se o `grep` não bastar.

**5. Busca local (qmd ou BM25 simples).**
Gatilho: `index.md` passa de ~300 linhas, ou você percebe a IA sem achar página que existe.
Ganho: recuperação deixa de depender do índice caber no contexto.

**6. Calibrar a escada de revisão.**
Gatilho: 3+ meses de uso, dados reais suficientes.
Ganho: intervalos ajustados ao seu esquecimento real, por conceito. Só depois de haver
histórico — antes disso, seria matemática sobre nada.

**7. Skill `/estudar` do Claude Code.**
Gatilho: você notar que a IA às vezes começa a sessão sem ler `INICIO.md`.
Ganho: gatilho explícito reforçando o protocolo. Custo: um arquivo global a manter.

**Deliberadamente fora do roadmap:** embeddings/vector DB (a busca por nome basta nesta
escala), agentes múltiplos (uma conversa, um estado), automação de ingest (a curadoria é sua e
é o passo mais valioso), app próprio (o valor está nos `.md`, não na interface).

---

## 6. Checagem contra os requisitos do briefing

| Requisito (seção 20 do briefing) | Onde |
|---|---|
| 1. Receber fontes | `RAW/<disciplina>/` + INGEST |
| 2. Transformar em conhecimento estruturado | INGEST → `KNOWLEDGE/` |
| 3. Criar links entre conceitos | `## Relacionado` obrigatório + `mapa-<disciplina>` |
| 4. Registrar meu conhecimento | `LEARNER/estado-<disciplina>.md` |
| 5. Perguntas adaptativas | TEACH §4 do `CLAUDE.md`, calibrado por estado |
| 6. Registrar erros e lacunas | evidências e confusões por conceito |
| 7. Planejar revisões | escada de níveis, campo `revisar:` |
| 8. Continuar sessão anterior | `INICIO.md` + LEARNER |
| 9. Atualizar memória após a sessão | UPDATE, com escrita incremental (#4) |

Perguntas da seção 22 do briefing — todas respondíveis lendo `INICIO.md` + `LEARNER/`, exceto
"quais fontes já estudei" (`index.md` / `mapa`) e "quais conceitos estão conectados"
(graph view do Obsidian ou seção `## Relacionado`).
