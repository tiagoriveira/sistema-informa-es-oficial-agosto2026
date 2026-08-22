# FAQ — uso cotidiano

Perguntas práticas do dia a dia. Regras do sistema: `CLAUDE.md`. Decisões de projeto e
limitações: [[ARQUITETURA]]. Formato das páginas: [[schema]].

---

## Começando

**Como eu começo, do zero?**
1. Crie `RAW/<disciplina>/` e coloque a primeira fonte lá dentro.
2. Abra o Claude Code Desktop nesta pasta.
3. Diga: **"ingere a fonte `RAW/economia/mankiw-cap-5.pdf`"**.
4. Confira a lista de conceitos que eu proponho, corte o que não interessa, aprove.
5. Diga: **"vamos estudar economia"**.

Você não precisa preencher nada à mão. `LEARNER/perfil.md` se preenche ao longo das primeiras
sessões — se quiser adiantar, responda nele por que você está estudando e qual o prazo.

**Preciso instalar algo?**
Obsidian (para ler e ver o grafo) e o Claude Code Desktop (a IA). Nenhum plugin. Git é
opcional e recomendado — ver "Manutenção".

**A IA não está seguindo as regras do sistema.**
Ela precisa estar aberta **nesta pasta**, porque o `CLAUDE.md` da raiz é carregado
automaticamente. Se a sessão está longa, as regras podem escapar: diga "releia o CLAUDE.md"
ou comece uma sessão nova. Sessão nova não perde memória — a memória está no vault, não no chat.

---

## Fontes

**Como adiciono uma fonte nova?**
Copie o arquivo para `RAW/<disciplina>/` e diga "ingere essa fonte". Não crie página à mão,
não organize `KNOWLEDGE/` você mesmo. A pasta da disciplina é criada no primeiro ingest.

**E se for um livro de 400 páginas?**
Um capítulo por vez: *"ingere o capítulo 5 do Mankiw, páginas 89 a 108"*. Resumir um livro
inteiro numa passada produz síntese genérica, boa para parecer completa e inútil para ensinar.
Vale mais um capítulo bem ingerido que dez rasos.

**E vídeo, aula, podcast?**
Salve a transcrição como `.md` em `RAW/<disciplina>/`. Áudio e vídeo não são lidos direto.

**Posso adicionar minhas próprias anotações como fonte?**
Pode, mas identifique: `RAW/economia/minhas-notas-aula-3.md`. Elas entram como fonte de
autoridade menor — se conflitarem com o livro, o livro ganha, e a divergência é registrada.

**Uma fonte serve a duas disciplinas.**
Guarde na principal e peça para a página de fonte referenciar a outra. Não duplique o arquivo:
duas cópias divergem, e aí não há mais fonte da verdade.

**Como sei o que já ingeri?**
`SYSTEM/index.md`, seção Fontes de cada disciplina. Ou:
```bash
grep "^## \[" SYSTEM/log.md | grep ingest
```

---

## Sessões de estudo

**Como começo uma sessão?**
"Quero estudar economia" ou só "continue". Eu leio `INICIO.md` e `LEARNER/estado-economia.md`,
digo em uma linha o que escolhi fazer e por quê, e explico direto — sem pergunta de abertura.

**Por que você não me faz pergunta?**
Por padrão, entrega vem antes de teste: friccão zero, sem pergunta de abertura, um
micro-conceito por vez. Avaliação (a pergunta que testa se você sabe) é um momento à parte —
só acontece quando há revisão vencida, quando você pede, ou quando você sinaliza que quer modo
ativo. Fora desses momentos, nada do que for só explicado conta como evidência de que você
sabe — ler/ouvir não é saber, então o conceito não muda de estado até ser de fato testado.
Se quiser ser testado a qualquer momento, é só pedir.

**Como peço para continuar de onde paramos?**
Só "continue". Não precisa resumir a sessão passada nem lembrar de nada — é justamente esse
trabalho que o sistema elimina. Se eu começar do zero um assunto já estudado, é bug: mande eu
ler o `INICIO.md` e o LEARNER.

**Quanto tempo deve durar uma sessão?**
20 a 45 minutos, um assunto por vez. Sessão de 3 horas cobrindo 5 tópicos gera registro raso e
aumenta a chance de eu perder o fio das regras.

**Como encerro?**
"Fecha a sessão". Eu gravo a nota de sessão, recalculo as datas de revisão, reescrevo o
`INICIO.md` e registro no log.

**E se eu fechar a janela sem encerrar?**
Você perde só a narrativa da sessão. O estado dos conceitos é gravado logo depois de cada
avaliação, não no fim (decisão #4 da [[ARQUITETURA]]). Na próxima vez, diga o que aconteceu e
eu completo o registro.

**Posso estudar duas disciplinas na mesma sessão?**
Pode, mas gera duas notas de sessão e costuma render menos. Prefira alternar entre dias.

**Em que ordem estudo disciplinas do mesmo hub?**
Siga a sequência mostrada na página de entrada do hub, em `SYSTEM/index.md` e na tabela do
`INICIO.md`: pré-requisitos primeiro, depois a disciplina que integra o assunto e, por fim,
as aplicações. Você pode pedir um desvio, mas eu devo dizer qual pré-requisito foi adiantado
ou deixado para depois e por quê.

---

## Corrigindo o sistema

**A IA registrou algo errado sobre mim. Como corrijo?**
Diga na conversa: *"você me marcou como frágil em elasticidade, mas eu errei porque li rápido —
me pergunta de novo"*. Eu reavalio de verdade (com uma pergunta, não na sua palavra) e corrijo
o registro. Correção também vira evidência datada — o histórico não é apagado, é atualizado.

**Posso editar os arquivos à mão?**
Pode, todos. É markdown, é seu. Duas ressalvas: (1) `RAW/` não deve mudar nunca; (2) se editar
o `LEARNER/`, avise na sessão seguinte — senão eu posso reescrever por cima com base numa
leitura anterior.

**Marquei um conceito errado como consolidado e agora ele sumiu da revisão.**
Diga *"tira consolidado de X e me testa"*. Se falhar, volta para nível 1 e reentra na fila.

**A IA escreveu uma página de conceito ruim.**
Diga o que está errado. Eu reescrevo, e a mudança vale para as próximas sessões porque ela lê
a página, não a nossa conversa. Se a página não deveria existir, peça para apagar e para
remover as referências — página apagada com links pendurados é pior que página ruim.

**Como sei se o `INICIO.md` está certo?**
Ele é derivado. Se discordar do `LEARNER/`, o LEARNER está certo — peça um lint e eu regenero.

---

## Fontes conflitantes

**Duas fontes discordam. O que acontece?**
Eu registro as duas na seção `## Divergências entre fontes` da página do conceito, com página
e citação, e sinalizo. Eu não escolho um lado sozinho — quem decide a autoridade pedagógica é
você.

**Como eu resolvo a divergência?**
Três caminhos: (1) *"a fonte A tem prioridade nesta disciplina"* — vira regra registrada no
mapa da disciplina e passa a valer; (2) *"mantém as duas"* — legítimo, e em muitos assuntos é
o mais honesto; (3) *"procura uma terceira fonte"* — você traz, eu ingiro, a divergência é
reavaliada.

**E se a fonte contradiz o que você sabe?**
Eu digo que discordo e por quê, mas ensino pela fonte, marcando minha objeção como
conhecimento externo. A fonte é a autoridade pedagógica; minha discordância é informação, não
veredito.

**Posso ter divergência entre a fonte e o que eu penso?**
Pode, e vale registrar — é aprendizado real. Peça para anotar como sua posição na página do
conceito, identificada como sua.

---

## Notas e páginas

**Quando uma página nova deve ser criada?**
Quando o conceito (1) tem nome próprio, (2) é reutilizável em mais de um contexto e (3) cabe
em uma frase. Os três, não dois.

**Quando não criar?**
- Exemplo ou caso particular → entra como exemplo na página do conceito.
- Detalhe específico de uma fonte → fica na página da fonte.
- Outro nome para algo que já existe → atualiza a página existente e registra o sinônimo.
- Você não consegue dizer a ideia central em uma frase → ou são dois conceitos, ou você ainda
  não entendeu o suficiente para ter uma página.

Na dúvida, não criar. É mais fácil criar depois do que perceber, seis meses adiante, que três
páginas dizem a mesma coisa com nomes diferentes.

**Onde salvo uma ideia?**
Em `ideias/`. Ela fica ali enquanto estiver em maturação, sem compromisso ativo. Quando ganhar
prazo e objetivo, vira `PROJETOS/`; se se tornar responsabilidade contínua, `AREAS/`;
referência externa é `RECURSOS/`.

**Onde salvo uma tarefa? Ou uma nota rápida qualquer?**
Em `TAREFAS.md`, na raiz do vault — home única (criada em 2026-08-22, depois de 4 arquivos de
tarefa soltos em paralelo causarem context switching; ampliada no mesmo dia pra também servir de
captura rápida). Toda tarefa nova, nota solta, ideia de passagem — venha de captura, de brain
dump ou de uma sessão — entra ali, sem precisar decidir a categoria na hora. Organização vem
depois. Se a tarefa virar um esforço com prazo e várias etapas, aí sim vira `PROJETOS/`; nota
crua longa ainda pode ir pro `INBOX/`, mas nada obriga mais.

**Posso arquivar uma resposta boa como página?**
Deve. Uma comparação, uma síntese, uma conexão que apareceu na conversa — se é reutilizável,
peça para virar página. É o mecanismo que faz suas perguntas acumularem, não só suas fontes.

**Preciso aprovar toda escrita?**
Não. Páginas em `KNOWLEDGE/` e memória (LEARNER, sessões, log, INICIO) são criadas ou
atualizadas automaticamente quando atenderem aos critérios do sistema. Você continua podendo
pedir para revisar, mover ou remover uma página depois.

---

## Progresso e revisão

**Como vejo meu progresso?**
- Agora: `INICIO.md`.
- Numa disciplina: `LEARNER/estado-<disciplina>.md`, os blocos por conceito.
- Ao longo do tempo: `SESSIONS/` em ordem, ou `grep "^## \[" SYSTEM/log.md`.
- Perguntando: *"o que mudou no meu conhecimento de economia neste mês?"*

**Não tem gráfico nem porcentagem?**
Não, por decisão de projeto — número inventado vira fato na sessão seguinte. Você tem quatro
estados com critério verificável e as evidências datadas que os justificam. Você pode discordar
de um estado apontando a evidência; de uma porcentagem, não.

**O que revisar hoje?**
Pergunte, ou abra o `INICIO.md`, ou:
```bash
grep -rn "revisar:" LEARNER/
```

**Como funcionam as revisões espaçadas?**
Cada conceito avaliado ganha um nível (1 a 5) e uma data. Acertou sem ajuda → sobe um nível e
a próxima revisão fica mais distante (1, 3, 7, 16, 35 dias). Acertou com hesitação → mantém.
Errou → volta para o nível 1. Confundiu com outro conceito → volta para 1 e os dois passam a
ser perguntados **lado a lado**, porque confusão isolada não se resolve.

**Perdi as revisões, estão todas vencidas.**
Normal, e não é para zerar de uma vez. Eu pego as 3 a 5 mais críticas (frágeis e antigas) e
reagendo o resto. Vencido não expira: um conceito atrasado só cai de nível se você errar.

**Posso pedir só revisão, sem conteúdo novo?**
"Hoje só revisão." Bom hábito uma vez por semana.

---

## Higiene do vault

**Como evito poluir o vault?**
1. Não crie página à mão — deixe o ingest e as sessões criarem.
2. Recuse conceitos na lista do ingest. Ingest que cria 40 páginas de uma fonte está errado;
   5 a 12 é a faixa saudável.
3. Não deixe conceito órfão: se nada aponta para a página, ou ela ganha um link no mapa, ou
   não deveria existir.
4. Um assunto, um nome. Se aparecer "elasticidade-preço" e "elasticidade de preço", una.
5. Lint a cada ~10 sessões.

**Como mantenho a memória da IA consistente?**
- Uma sessão por vez (não duas janelas no mesmo vault ao mesmo tempo).
- Encerre com "fecha a sessão" quando der.
- Corrija registro errado na hora, não depois.
- Se editar o LEARNER à mão, avise.
- Confie no `LEARNER/`, não no `INICIO.md`, quando os dois discordarem.
- Sessões curtas. Sessão longa aumenta a chance de eu perder o protocolo.

**Assunto completamente novo, sem fonte nenhuma. E aí?**
Duas opções, e vale escolher conscientemente:
- **Com fonte (recomendado):** traga uma fonte primeiro, mesmo que um artigo só. O sistema foi
  desenhado para ter autoridade pedagógica externa; sem isso, você está estudando pela memória
  de um modelo, sem verificação.
- **Sem fonte (exploração):** eu ensino do meu conhecimento, mas **tudo** fica marcado como
  conhecimento externo, e a disciplina fica sinalizada como sem fontes no mapa. Serve para
  reconhecer terreno e decidir o que ler depois. Quando a fonte chegar, o ingest confirma ou
  corrige o que foi escrito — e as correções são registradas.

**Como verifico se você está usando minhas fontes de verdade?**
- Toda afirmação em `KNOWLEDGE/` deve ter `(cf. [[fonte]], p. X)`. Sem citação = não é da fonte.
- Pergunte no meio da sessão: *"isso está na minha fonte? onde?"* Resposta boa cita página.
- Confira por amostragem: abra a página, abra o PDF na página citada, compare. Faça isso nas
  duas ou três primeiras ingestões de cada fonte nova — é o teste de calibragem que mais paga.
- Procure o que não deveria existir:
  ```bash
  grep -rn "Conhecimento externo" KNOWLEDGE/    # deve ser raro e sempre rotulado
  grep -rLn "cf\. \[\[" KNOWLEDGE/*/*.md        # páginas de conceito sem nenhuma citação
  ```
- Se eu ensinar algo que não está na fonte sem avisar, aponte. É violação de regra, não estilo.

---

## Manutenção

**Com que frequência?**
- A cada ~10 sessões: **"roda um lint"**. Eu reporto os problemas antes de corrigir nada.
- A cada ~3 meses: leia o `CLAUDE.md` e ajuste as regras que não estão funcionando para você.
  Ele é seu, não é imutável.
- A cada ~6 meses: releia `LEARNER/perfil.md`. Seus objetivos mudam.
- Virada de ano: arquivar `log.md` como `log-2026.md`.

**O que o lint verifica?**
Links quebrados, páginas órfãs, conceitos citados sem página, duplicatas, contradições,
conceitos em KNOWLEDGE que nunca entraram no LEARNER, conceitos sem revisão agendada, revisões
muito atrasadas, sessões que não mudaram estado nenhum, e `INICIO.md`/`index.md` fora de
sincronia.

**Como ligo o Git?** (já ligado)
Já está ativo, com remoto no GitHub. Quando você diz que quer encerrar a sessão, eu faço
`git add` dos arquivos do vault que mudaram, `commit` com mensagem descrevendo a sessão, e
`push` — automático, sem precisar pedir. Ganho: desfazer qualquer corrupção e ver o histórico
real de mudanças, sincronizado. Se quiser fazer manual em algum momento, o comando é
`git add -A && git commit -m "sessao $(date +%F)" && git push`.

**Backup?**
O OneDrive já sincroniza. Para algo importante de verdade, Git + um remoto privado.

**O vault cresceu e a IA está lenta ou perdida.**
Gatilhos objetivos em [[ARQUITETURA]] §5: LEARNER acima de ~300 linhas → dividir por tema;
`index.md` acima de ~300 linhas → considerar busca local.

---

## Erros comuns

| Erro | Por que dói | O que fazer |
|---|---|---|
| Ingerir 10 fontes antes de estudar qualquer coisa | vira biblioteca de resumos que você não leu; KNOWLEDGE grande e LEARNER vazio | uma fonte, estude, depois a próxima |
| Dizer "entendi" para acelerar | envenena o modelo do aluno; ele te poupa justamente do que você precisa | diga "não entendi" sem economia — é a informação mais útil que você me dá |
| Pedir a explicação antes de tentar responder | você troca aprendizado por conforto | tente, mesmo errado. O erro é o dado |
| Nunca encerrar a sessão | perde a nota de sessão e as datas de revisão | "fecha a sessão", ou avise na vez seguinte |
| Criar páginas à mão em `KNOWLEDGE/` | fica fora do índice, fora do mapa, órfã | peça para mim, ou avise para eu indexar |
| Mexer no `RAW/` | quebra as citações de página das fontes | RAW é imutável. Fonte nova = arquivo novo |
| Aceitar toda página que eu proponho | 40 páginas rasas por fonte, ninguém revisita | corte na lista. Faixa saudável: 5 a 12 |
| Estudar sem fonte por meses | você estuda a memória de um modelo, sem verificação | traga fonte, ou aceite conscientemente o modo exploração |
| Duas janelas do Claude no mesmo vault | uma sobrescreve a memória da outra | uma sessão por vez |
| Confiar no `INICIO.md` contra o `LEARNER/` | o INICIO é cache; pode estar velho | LEARNER vence sempre |
| Sessão de 3 horas cobrindo tudo | registro raso, protocolo se perde | 20 a 45 min, um assunto |
| Deixar tudo para "o lint resolve" | o lint reporta, mas não inventa a evidência que ninguém registrou | corrija na hora |

---

# Boas práticas recomendadas

## Do briefing, na prática

**1. Uma fonte por vez, e estude antes de ingerir a próxima.**
O valor do sistema está no ciclo completo — ingerir, estudar, errar, revisar. Ingerir dez
fontes antes de estudar uma constrói uma biblioteca de resumos que você nunca leu.

**2. Quando eu te testar, responda antes de pedir a resposta.** Mesmo com certeza de que vai
errar. Um erro diagnosticado vale mais que três explicações lidas — e é a única forma de o
sistema saber o que ensinar. (Fora do momento de teste, a entrega já vem direta — não é
preciso pedir.)

**3. Diga "não entendi" sem constrangimento.** É a informação mais valiosa que você produz.
"Entendi" para acelerar corrompe o modelo por meses.

**4. Corte na lista de conceitos do ingest.** Você é o curador. Cinco páginas que você vai
revisitar valem mais que trinta que você nunca vai abrir.

**5. Confira as citações nas primeiras ingestões de cada fonte.** Abra o PDF na página citada
e compare. Duas ou três amostras bastam para calibrar a confiança — e para pegar cedo o modo
de falha mais caro do sistema.

## Práticas que não estavam no briefing

**6. Faça uma "sessão zero" por disciplina, antes de qualquer fonte.**
Deixe eu te perguntar o que você já acha que sabe sobre o assunto. Registra estado inicial
honesto, revela concepções erradas que você já traz (as mais difíceis de corrigir depois, e as
que mais atrapalham), e torna visível a evolução dos primeiros meses. Dez minutos, uma vez por
disciplina. **Diga: "faz uma sessão zero de economia comigo".**

**7. Peça a decisão pedagógica em voz alta.**
Eu devo abrir a sessão dizendo o que escolhi fazer e por quê ("vou revisar elasticidade antes
de avançar, porque você errou na quinta e vence hoje"). Se eu não disser, peça. Isso te deixa
discordar da estratégia — e é a sua principal janela para auditar se eu li a memória mesmo ou
estou improvisando.

**8. Use o "teste do dia seguinte" antes de aceitar `consolidado`.**
Se você quer confiar no rótulo, peça a recuperação no dia seguinte sem reler nada. Reconhecer
na hora é fácil; recuperar 24 horas depois é o que indica que ficou. O critério de
`consolidado` já exige isso — mas peça explicitamente quando o conceito for importante.

**9. Explique com suas palavras, não com as da fonte.**
Quando eu perguntar, evite reproduzir a formulação do livro. Reformular é o teste; repetir é
memória de curto prazo passando por compreensão.

**10. Registre suas próprias conclusões, marcadas como suas.**
Quando você chegar a uma conexão que a fonte não faz, peça para registrar identificada como
sua posição. Depois de meses, a diferença entre "o que li" e "o que concluí" é o ativo mais
valioso do vault — e é o que nenhum resumo de IA produz. (É o mesmo papel que a pasta
`insights/` cumpre no seu `vault-conhecimento-ia`.)

**11. Trate o `CLAUDE.md` como configuração viva.**
Se uma regra atrapalha, mude. Se você descobre um padrão que funciona ("sempre me dê um caso
concreto antes da definição"), escreva lá. É o único arquivo que muda meu comportamento em
todas as sessões futuras — anotar na conversa não muda nada, editar o `CLAUDE.md` muda tudo.

**12. Termine a sessão com uma pergunta em aberto, não com uma conclusão.**
Peça para eu registrar em "Próxima sessão" uma pergunta que você não conseguiu responder.
Começar com a tensão intacta vale mais do que começar com um resumo — e evita o problema
clássico de reabrir revisando o que já estava fácil.

**13. Estude no Obsidian com o grafo aberto ao lado.**
Ver o conceito novo se conectar ao que já existe é o feedback que faz o sistema parecer vivo,
e o que sustenta o hábito nos primeiros meses. Também é o jeito mais rápido de notar uma
região do grafo isolada — que quase sempre indica um assunto que você ingeriu e nunca estudou.

**14. Commit ao fim da sessão.**
Um comando. Você ganha desfazer para qualquer corrupção de memória e um segundo registro
histórico, independente do que eu escrevo. É a melhoria de maior retorno por esforço do
sistema inteiro.

**15. Estabeleça uma cadência mínima, não uma ideal.**
Duas sessões de 30 minutos por semana, sustentadas por um ano, valem mais que um plano diário
abandonado em três semanas. A repetição espaçada supõe que você aparece; um sistema que exige
mais do que você entrega gera fila vencida e culpa — e é assim que ele morre.
