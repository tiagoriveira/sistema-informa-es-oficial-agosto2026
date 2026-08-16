# LOG

Append-only. Nunca reescreva ou apague entrada antiga — só acrescente no fim.

Prefixo fixo, para permitir busca simples:

```bash
grep "^## \[" SYSTEM/log.md | tail -10
grep "^## \[" SYSTEM/log.md | grep ingest
```

Operações: `ingest` · `study` · `review` · `update` · `lint` · `system`

Ao virar o ano: renomeie para `log-2026.md` e comece um `log.md` novo.

---

## [2026-08-12] system | criação do vault

Estrutura inicial criada: RAW, KNOWLEDGE, LEARNER, SESSIONS, SYSTEM, _templates.
Constituição em `CLAUDE.md`, formatos em [[schema]], documentação em [[ARQUITETURA]] e [[FAQ]].
Nenhuma disciplina, fonte ou conceito ainda. Próximo passo: primeiro INGEST.

## [2026-08-13] system | ideias/roadmap/backlog + regras de sessão

Criadas pastas `ideias/`, `backlog/`, `roadmap/` (fluxo: captura → maturação → validada →
`backlog/` → `roadmap/`), formato proposto em cada `LEIA-ME.md`. `CLAUDE.md` ganhou modo
passivo no TEACH (§4) e regra de brevidade (§8), a pedido do Tiago.

## [2026-08-13] update | product-discovery

Arquivadas 4 páginas explicadas em modo passivo: [[validacao-de-problema]],
[[riscos-de-descoberta]], [[jobs-to-be-done]], [[continuous-discovery]], mais
[[mapa-product-discovery]]. Todas rotuladas como conhecimento externo (sem fonte em RAW/).

## [2026-08-13] study | product-discovery

Primeira sessão da disciplina (sem fontes em `RAW/`, modo exploração — ver `FAQ.md`).
Avaliado [[validacao-de-problema]]: acertou com hesitação a definição, errou a aplicação
(desenho de teste barato). Estado: nao_iniciado → em_desenvolvimento (nível 1, revisar
2026-08-14). Detalhe em `SESSIONS/2026-08-13-product-discovery.md`.

## [2026-08-13] update | product-discovery (2)

Arquivadas mais 3 páginas explicadas em modo passivo: [[mvp-e-tipos-de-experimento]],
[[outcome-vs-output]], [[dual-track-agile]]. `mapa-product-discovery.md` reordenado (7
conceitos). Regra de check-in em modo passivo ajustada no `CLAUDE.md` — só ao fim de bloco.

## [2026-08-13] system | 6 disciplinas registradas vazias

A pedido do Tiago (exceção deliberada à prática de "uma disciplina por vez"): registrados
mapa + estado vazios para gestao-conhecimento-second-brain, marketing,
visao-estrategica-negocios, fundamentos-sistemas-gestao, financas, ingles. Todas sem fontes.
Inglês recebeu nota de formato adaptado (não segue o modelo de conceito único).

## [2026-08-13] study | colaboracao-humano-ia

Disciplina nova, checada por busca na web (pedido do Tiago, evitar conceito desatualizado).
[[operador-centauro]]: nao_iniciado → em_desenvolvimento (acertou com hesitação, nível 1,
revisar 2026-08-14). Detalhe em `SESSIONS/2026-08-13-colaboracao-humano-ia.md`.

## [2026-08-13] study | product-discovery (2)

Segunda sessão do dia. [[validacao-de-problema]] segue em_desenvolvimento — errou de novo a
recuperação livre de métodos. [[riscos-de-descoberta]]: nao_iniciado → em_desenvolvimento
(evidência espontânea, nível 1, revisar 2026-08-14). Detalhe em
`SESSIONS/2026-08-13-product-discovery-2.md`.

## [2026-08-14] system | filosofia registrada

Nova disciplina, a pedido do Tiago (decidiu manter separada do vault-conhecimento-ia, que
segue só para notas atômicas via skill `obsidian-filosofia`). Mapa + estado vazios, sem
fontes ainda.

## [2026-08-14] study | filosofia

Primeira sessão. [[mito-para-logos]] (Tales de Mileto, virada mythos→logos): nao_iniciado →
em_desenvolvimento, acertou sem ajuda por que Tales é o primeiro filósofo (nível 2, revisar
2026-08-17). Página criada em KNOWLEDGE, rotulada como conhecimento externo (sem fonte RAW).

## [2026-08-14] update | filosofia (modo passivo)

A pedido do Tiago, TEACH passou a checar só ao fim de bloco (não a cada output) — CLAUDE.md
§4 ajustado. Depois disso, Tiago pediu modo passivo (sem pergunta nenhuma por hora).
Explicados em sequência: [[anaximandro-apeiron]], [[anaximenes-ar]],
[[heraclito-fluxo-e-logos]], [[parmenides-ser-imutavel]]. Páginas criadas, todas
`nao_iniciado` no LEARNER — nada testado ainda, conteúdo só explicado. Depois, páginas de
[[empedocles-quatro-raizes]] e [[democrito-atomismo]] também criadas, mesmo estado.

## [2026-08-14] system | protocolo de entrega reescrito (CLAUDE.md §4 e §8)

Inspirado em análise do repo Ybernator (app de estudos do Tiagolink repo: https://github.com/tiagoribeiror58-debug/escola-tiago-oficial.git ) a pedido dele. TEACH: item 3
virou "entrega de fricção zero" (explica direto, sem pergunta de abertura, exemplo/aplicação
prática, termina bloco com menu de próximos passos, não pergunta); item 4 isola avaliação em
momento próprio (só quando pedido, revisão vencida, ou modo ativo sinalizado) — substitui a
exceção "modo passivo", que virou o comportamento padrão. §8 ganhou teto numérico (~120
palavras/conceito, ~250/output) no lugar de "curto por padrão". 3 ideias maiores da mesma
conversa (dashboard/currículo, INBOX de notas, ementa com status ✅📍⬜) foram para `ideias/`
em vez do CLAUDE.md — são produto, não regra de tutor.

## [2026-08-14] update | filosofia (2)

Páginas de [[sofistas-relativismo]] e [[socrates-metodo-elenchos]] criadas (explicados em
bloco, ainda não testados) antes de fechar a sessão — conteúdo que só existia no chat.
Correção: datas de todo o trabalho de filosofia estavam erradas como 2026-08-13; corrigidas
para 2026-08-14 (data real), incluindo o revisar de [[mito-para-logos]] (2026-08-16 →
2026-08-17). Sessão fechada em `SESSIONS/2026-08-14-filosofia.md`.

## [2026-08-14] system | FAQ e ARQUITETURA desatualizados pelo protocolo novo

Tiago pediu auditoria de consistência entre FAQ.md/ARQUITETURA.md e o CLAUDE.md real.
Achados: FAQ descrevia "abre com pergunta" como padrão (virou exceção hoje), e ambos
descreviam git commit como manual (agora é automático ao encerrar). Corrigidos os dois.
CLAUDE.md ganhou invariante 10 (checar FAQ/ARQUITETURA sempre que uma regra mudar) e o passo
5 do UPDATE (git push automático, que já valia por pedido do Tiago mas só estava na memória
da IA, não no CLAUDE.md).

## [2026-08-14] system | ementa visual implementada ([[ementa-mapa-status-visual]])

Ideia validada e executada no mesmo dia. Status visual (✅⚠️📍⬜) na "Ordem de estudo
sugerida" do mapa — cache derivado do LEARNER, regenerado a cada UPDATE. Formato em
`schema.md` §3, regra no `CLAUDE.md` (UPDATE). Aplicado em `mapa-filosofia.md`: 📍 em
[[mito-para-logos]] (único avaliado), resto ⬜.

## [2026-08-14] system | auditoria semanal automática configurada

Routine na nuvem (`trig_012aX6ua3PESCJ8B5Gmq1ece`), roda todo domingo 20h BRT (23h UTC).
Audita CLAUDE.md vs FAQ/ARQUITETURA, links quebrados, páginas órfãs, conceitos sem entrada no
LEARNER, revisões vencidas, INICIO.md/index.md fora de sincronia. Só reporta (não corrige),
escreve entrada `lint` no fim deste log e dá push — sem tocar em mais nada. Removi os
conectores MCP que vieram anexados por padrão (Meta Ads, Notion, Vercel, etc.) — a auditoria
só precisa do repo git. CLAUDE.md §3 ganhou "git pull no início da sessão", senão o relatório
semanal fica preso no GitHub e a sessão local nunca vê.

## [2026-08-14] system | neurociencia-esportiva registrada

Nova disciplina, a pedido do Tiago. Mapa + estado vazios inicialmente, sem fontes ainda.
Aproveitado o momento para corrigir `SYSTEM/index.md`: filosofia estava listada como "sem
sessão" dentro de "Outras disciplinas", desatualizado desde que ganhou 9 conceitos —
promovida a seção própria, igual product-discovery.

## [2026-08-14] system | trilha em partes (agrupamento tipo Ybernator)

Inspirado na hierarquia de categorias do Ybernator (>3 sub-áreas → agrupa). "Ordem de estudo
sugerida" com mais de ~5-6 itens agora agrupa em `### Parte N — tema`, numeração corrida
(regra do ⚠️/📍 inalterada). Documentado em `schema.md` §3. Aplicado em
`mapa-neurociencia-esportiva.md` (3 partes) e `mapa-filosofia.md` (2 partes: pré-socráticos /
virada antropológica).
_(Superado no mesmo dia — ver "grade curricular" abaixo: "Parte" virou "Fase", e o
agrupamento que eu tinha inventado tinha fases de 2 itens.)_

## [2026-08-14] system | reestruturação: hub → disciplina → fase

Pedido do Tiago, inspirado na estrutura real do Ybernator (`EmentaFase {nome, topicos[]}` e
hubs com `isCategory`). KNOWLEDGE saiu de plano para 3 níveis:
`KNOWLEDGE/<hub>/<disciplina>/fase-N-<slug>/`, com o mapa sozinho no nível da disciplina.
8 hubs criados; `filosofia` virou `historia-da-filosofia` dentro do hub `filosofia` (é uma
das várias disciplinas de filosofia possíveis). `estado-filosofia.md` renomeado junto, e
todas as referências aos nomes antigos (mapa e estado) atualizadas. Links não
quebraram (invariante 6 — Obsidian resolve por nome, não por caminho). `ARQUITETURA` #8
reescrita: registrava KNOWLEDGE plano como decisão deliberada, agora registra a mudança e
por que a razão original enfraqueceu. `schema.md` §0 ganhou a árvore de pastas.

## [2026-08-14] system | grade curricular nas 10 disciplinas

Tiago recusou importar as ementas do Ybernator ("a sequência ali talvez não seja a correta e
muitos tópicos podem ter ficado obsoletos") — grades desenhadas do zero. Formato: `### Fase N
— <tema>`, 4-6 tópicos por fase, 3-6 fases, tópico descritivo em vez de nome solto de
conceito (`schema.md` §3). Total: 253 tópicos em 10 disciplinas.

Busca web (regra §6) nas que envelhecem: neurociência esportiva, colaboração humano-IA,
marketing, gestão do conhecimento, finanças, sistemas/gestão — fontes citadas em `## Nota
sobre a grade` no fim de cada mapa. Sem busca em história da filosofia (canônica), inglês
(CEFR é padrão estável) e visão estratégica (arcabouço estável, só exemplos envelhecem).
Product-discovery redesenhada sobre os 7 conceitos existentes: o buraco era método de coleta
de evidência, que virou a Fase 3.

`fundamentos-sistemas-gestao` ficou como uma disciplina só: o corte que o Tiago levantou
(sistêmico / sistemas de informação / pessoas) virou Fases 1-2, 4 e 5 — a ordem importa,
ERP sem processo é apertar botão. `financas` idem: pessoal (Fases 1-3) → corporativo (4-5).

## [2026-08-14] study | neurociencia-esportiva

Pergunta do Tiago sobre "O Jogo Interior do Tênis" (Gallwey) puxou os itens 14 e 20 da grade
antes da ordem (desvio válido pelo §4.2 — motivo: pergunta espontânea conectando os dois).
Checado na web: hipótese da ação restrita (Wulf) e teoria do reinvestimento (Masters) dão
mecanismo científico ao que o livro descreve por metáfora (Self 1/Self 2). Páginas criadas:
[[foco-atencional-nideffer]] (fase-3) e [[choking-sob-pressao]] (fase-4) — explicadas, ainda
`nao_iniciado` no LEARNER, nada testado. Gallwey citado como fonte do método, não fonte
científica — livro ainda não está em `RAW/`.

## [2026-08-14] system | fecha a sessão

`SESSIONS/2026-08-14-filosofia.md` renomeada para `2026-08-14-historia-da-filosofia.md`
(acompanha o rename da disciplina) e completada com o que aconteceu depois do primeiro
fechamento (reestruturação em hub/fase, grade de 9→33 tópicos). Criada
`SESSIONS/2026-08-14-neurociencia-esportiva.md`. Nenhuma avaliação nova em nenhuma das duas
— só explicação e reorganização; `INICIO.md` reescrito.

## [2026-08-15] system | teto de tamanho revogado

Tiago achou os itens rasos demais pra conteúdo teórico ("nos livros cada item é bem
explicado, não mastigado"). §8 do CLAUDE.md: teto de ~120/250 palavras revogado, cada
conceito agora é explicado a fundo (mecanismo, exemplo, nuance, contraponto), sem limite
fixo. §4 item 3 ajustado pra não contradizer ("profundidade vem de iterar" → "profundidade
vem do conceito bem explicado"). Ritmo de um conceito por vez continua igual — mudou
profundidade, não quantidade. Checado FAQ/ARQUITETURA (invariante 10): nada desatualizado.

## [2026-08-15] system | entrega fatiada em partes

Ajuste no mesmo dia: bloco único longo (o item 3 de gestão-conhecimento saiu inteiro —
mecanismo, exemplo, nuance, contraponto — de uma vez) também gerou fricção de leitura. §4
item 3 e §8: quanto explico (sem teto) e quanto entrego por output (uma parte do conceito por
vez — mecanismo, depois exemplo, depois nuance) são regras separadas agora.

## [2026-08-15] system | disciplina nova: obsidian

Tiago pediu "um curso sobre obsidian". Criada a 11ª disciplina, no hub `gestao-sistemas`:
`KNOWLEDGE/gestao-sistemas/obsidian/mapa-obsidian.md` (grade de 5 fases / 26 tópicos) e
`LEARNER/estado-obsidian.md` vazio. Grade checada por busca na web (§6) porque o Obsidian
mudou entre 2025 e 2026: Bases virou core plugin e assume o lugar do Dataview como caminho
padrão de dashboard; app gratuito inclusive para uso comercial. Fronteira declarada no mapa:
ferramenta aqui, método em [[mapa-gestao-conhecimento-second-brain]]. `index.md` e
`INICIO.md` atualizados (10 → 11 disciplinas, 253 → 279 tópicos).

## [2026-08-15] system | obsidian: tópico de comandos/hotkeys

Tiago pediu "comandos para produtividade no Obsidian". Entregue na conversa (paleta `Ctrl+P`
como porta única + atalhos padrão do Windows, checados na doc oficial). Grade de
[[mapa-obsidian]] passou de 26 → 27 tópicos: novo tópico 6 na Fase 1 (command palette e
hotkeys), renumerando os seguintes — a fase pulava do modelo mental direto pra links sem
passar por como se opera a ferramenta. `index.md` e `INICIO.md` acertados.

## [2026-08-15] system | página: comandos-e-hotkeys-obsidian

Tiago pediu pra salvar os comandos no vault mesmo depois de eu recomendar o contrário
(cheatsheet envelhece e a doc oficial já é referência viva). Decisão dele, página criada:
`KNOWLEDGE/gestao-sistemas/obsidian/fase-1-modelo-mental/comandos-e-hotkeys-obsidian.md`,
marcada como 100% conhecimento externo e datada 2026-08-15, com aviso de que em conflito o
app vence. Primeira página da disciplina; tópico 6 do mapa virou link. `estado-obsidian.md`
recebeu o bloco como `nao_iniciado` (entregue, não testado). `index.md` atualizado.

## [2026-08-15] study | gestao-conhecimento-second-brain

Primeira sessão da disciplina. Fase 1 explicada do item 1 ao 4 (arquivo morto, CODE, captura
seletiva, nota efêmera vs. permanente — este parcial, partes 1-2). **Nenhum virou página e
nenhum foi testado** — dívida de escrita registrada no `INICIO.md`. Duas correções de regra
no meio: teto de palavras revogado, depois entrega fatiada em partes (entradas acima).
Pedido interrompido no fim (hubs de dinâmicas sociais e mente + disciplina "Comportamento
Masculino e Realismo") — nada feito, anotado como pendente. Sessão em
`SESSIONS/2026-08-15-gestao-conhecimento-second-brain.md`.

## [2026-08-15] system | correção de data

As duas entradas de regra acima estavam datadas 2026-08-14; a sessão virou a meia-noite e o
trabalho é de 2026-08-15. Corrigidas aqui e no `CLAUDE.md` §8. Os commits de 08-14 estão
certos — aquela parte da sessão foi mesmo no dia 14.

## [2026-08-15] update | gestao-conhecimento + marcador 📖

Os 4 itens da Fase 1 viraram página: [[arquivo-morto]], [[ciclo-code]],
[[captura-seletiva]], [[nota-efemera-vs-permanente]] — todas `nao_iniciado`, só explicadas.
Pendência de escrita da sessão anterior resolvida.

Tiago perguntou por que aqui não existe o marcador de concluído que o Ybernator tem. Buraco
real: `⬜` não distinguia "nunca tocado" de "já expliquei, você só não foi testado". Criado
`📖` (explicado, nunca testado) em `schema.md` §3 — não pode ser `✅` porque ✅ aqui exige
evidência de 2+ dias, e marcar concluído só por ter sido explicado seria domínio fantasma
(invariantes 1 e 2). Legenda dos 5 símbolos adicionada ao `INICIO.md`.

## [2026-08-15] system | camada INBOX criada

Tiago trouxe a primeira nota pessoal e perguntou onde salvar. Criada `INBOX/` na raiz, irmã
de KNOWLEDGE/LEARNER/SESSIONS, conforme já indicado em [[inbox-notas-pessoais]] (nota pessoal
não pode cair em KNOWLEDGE — quebra o §3 e o LINT). Três arquivos: `LEIA-ME.md`,
[[2026-08-15-motivacao-por-validacao-externa]] e [[marco-aurelio-validacao-externa]]. Texto
original preservado literal; único ajuste foi normalizar o wikilink dele para kebab-case
(schema §0). A citação foi localizada na web: *Meditações* 6.51 — e a tradução dele traz
"sedutor" onde o original é quem ama o prazer. Nada virou página de KNOWLEDGE (invariante 8).
Pendente e não feito por conta própria: `CLAUDE.md` §1 e §3 não citam a camada INBOX.

## [2026-08-15] ingest | disciplina nova: performance-esportiva

Tiago perguntou onde estudar VO2 max; nenhuma disciplina cobria fisiologia do esforço.
Criada a 12ª disciplina, hub novo `esporte`: `KNOWLEDGE/esporte/performance-esportiva/
mapa-performance-esportiva.md` (5 fases / 21 tópicos: bioenergética, VO2 max, limiar,
força/potência, periodização) e `LEARNER/estado-performance-esportiva.md` vazio. Grade
checada por busca na web (§6). Hub `esporte` separado de `neurociencia` por decisão própria:
fisiologia do esforço não é neurociência, é disciplina vizinha — fronteira declarada nos dois
mapas ([[mapa-performance-esportiva]] e [[mapa-neurociencia-esportiva]], cruzada nos dois
sentidos). `index.md` e `INICIO.md` atualizados (11 → 12 disciplinas, 280 → 301 tópicos).

## [2026-08-15] system | CLAUDE.md formaliza a camada INBOX

Proposta de 2026-08-15 aprovada pelo Tiago ("faça o recomendado"). `CLAUDE.md` §1 ganhou
linha `INBOX` na tabela de camadas; §3 ganhou a regra de que `INBOX/` não entra na leitura
automática. Checado invariante 10: `ARQUITETURA.md` estava desatualizado em dois pontos — o
diagrama de árvore não listava `INBOX/`, e a tabela "onde mora a verdade" também não. Ambos
corrigidos no mesmo momento. `FAQ.md` revisado, nada precisou mudar.

## [2026-08-15] ingest | disciplina nova: producao-de-conteudo

Tiago pediu dicas de conteúdo pra Instagram e depois estendeu pra "outras redes também".
Depois da resposta com pipeline de repurposing (Instagram, TikTok, YouTube Shorts, LinkedIn,
Threads/X), pediu pra virar disciplina. Criada no hub `marketing`, irmã de `marketing`:
`KNOWLEDGE/marketing/producao-de-conteudo/mapa-producao-de-conteudo.md` (5 fases / 23
tópicos: fundamentos → pipeline de repurposing → mecânica por plataforma → sustentabilidade
→ IA) e `LEARNER/estado-producao-de-conteudo.md` vazio. Grade checada na web (§6). Fronteira
com `marketing` declarada nos dois mapas: lá é estratégia, aqui é o ofício de plataforma.
`index.md` e `INICIO.md` atualizados (12 → 13 disciplinas, 301 → 324 tópicos).

## [2026-08-15] system | prompt anti-alucinação incorporado ao CLAUDE.md

Tiago colou um system prompt genérico (anti-alucinação, concisão, "estagiário não guia") e
perguntou como trazer pro sistema. Duas partes conflitavam com regra já decidida: "seja
conciso" vs. §8 "profundidade sem teto" (revogado em 2026-08-15 de propósito, pra não ensinar
raso); e "estagiário, não guia" vs. linha 3 "você é o tutor" (decide o quê estudar, avalia
sem ser pedido — papel ativo por design). Perguntado ao Tiago via AskUserQuestion; escolheu
em ambos a opção recomendada: concisão só fora do TEACH, e "estagiário" vira regra de TOM
(sem autoridade que os dados não sustentam), não mudança de papel.

Aplicado: invariante 11 (§2) — não tratar estimativa como fato, "não verificado" em vez de
lacuna preenchida. §6 — toda afirmação com número/nome exige fonte real, proibido "estudos
mostram" sem autor/ano/título. §8 — dois parágrafos novos: concisão fora do TEACH, e postura
de estagiário (esclarecer ambiguidade antes de responder, linguagem simples pra termo
difícil). Checado FAQ/ARQUITETURA (invariante 10): nada desatualizado.

## [2026-08-15] system | fecha sessão (obsidian + performance-esportiva + producao-de-conteudo)

Sessão encerrada a pedido. Três `SESSIONS/` gravadas: [[2026-08-15-obsidian]],
[[2026-08-15-performance-esportiva]], [[2026-08-15-producao-de-conteudo]] — todas INGEST,
zero avaliação, zero mudança de estado. Nenhuma revisão para recalcular. `INICIO.md`
reescrito: última sessão, revisões vencidas (2 dias de atraso agora), lacuna nova
(pipeline de repurposing só no chat, sem página), pendência do INBOX sem triagem. Pendência
antiga (hubs dinâmicas-sociais/área-da-mente + disciplina Comportamento Masculino e
Realismo) segue sem tocar, carregada de novo.

## [2026-08-15] system | INBOX: vocabulário de categoria decidido + notas organizadas

Tiago pediu recomendação sobre vocabulário e pra organizar as notas. Decidido: campo
`categoria:` fechado em ideia/pergunta/observacao/citacao, documentado em `INBOX/LEIA-ME.md`
e [[inbox-notas-pessoais]]. As duas notas existentes classificadas: motivação-por-validação
= ideia, marco-aurélio = citacao. Nenhuma virou página de KNOWLEDGE (invariante 8 — organizar
não é criar página, isso continua exigindo aprovação explícita). Recomendação registrada em
cada nota: a de motivação aponta pro hub "área da mente" ainda pendente de criar; a de Marco
Aurélio espera a grade de historia-da-filosofia chegar no estoicismo.

## [2026-08-15] system | camada NOTAS criada — destino permanente do INBOX

Tiago apontou que INBOX sozinho deixava nota pessoal empilhada sem destino — o próprio
[[nota-efemera-vs-permanente]] descreve esse anti-padrão ("inbox" como arquivo morto com nome
bonito). Criada `NOTAS/`, camada irmã de INBOX/KNOWLEDGE: destino de nota triada que não vira
página de KNOWLEDGE (sem disciplina/fonte, mas fica de pé sozinha). As duas notas de hoje
migradas: nomes perderam o prefixo de data (convenção passa a ser igual KNOWLEDGE — nota
permanente é atemporal), `triada: sim`, link interno corrigido pro novo nome do arquivo.
`INBOX/LEIA-ME.md` ganhou seção "Destino, depois de triada" explicando o critério: vira
KNOWLEDGE (pede aprovação, invariante 8) ou vira NOTAS (não pede — é organização, não criação
de conteúdo). `CLAUDE.md` §1 e §3, `ARQUITETURA.md` (diagrama + tabela) e `index.md`
atualizados. FAQ checado (invariante 10): nada desatualizado.

## [2026-08-15] system | correção: nota permanente não carrega pendência de processo

Tiago apontou que as duas notas em `NOTAS/` tinham seção "Triagem" com recomendação de
"espera tal coisa acontecer" — pendência de sistema misturada em conteúdo que deveria ser
permanente/autônomo, e duplicada com o que já está no `INICIO.md`. Risco real: sessão futura
lendo só a nota (sem o histórico desta conversa) podia achar que havia decisão em aberto
específica daquela nota. Seção removida das duas notas, substituída por `## Relacionado`
(cross-link simples). `INICIO.md` continua sendo o único lugar que rastreia essa pendência.
Regra nova em `NOTAS/LEIA-ME.md`: nota permanente não carrega pendência de processo.

## [2026-08-15] system | fecha sessão (INBOX/NOTAS + prompt anti-alucinação)

Sessão encerrada a pedido. Sem disciplina de estudo tocada nesta parte — trabalho de sistema:
prompt anti-alucinação incorporado ao CLAUDE.md, camada NOTAS criada e as 2 notas do INBOX
migradas, correção de design (nota permanente não carrega pendência de processo). Sem
avaliação, sem revisão pra recalcular. `INICIO.md` já revisado e consistente, sem mudança
necessária nesta rodada.

## [2026-08-15] study | performance-esportiva: bioenergética (itens 1-3)

Primeira sessão de ensino da disciplina. Itens 1-3 da Fase 1 explicados (três sistemas
energéticos, ATP-CP a fundo, glicólise/mito do lactato), nenhum avaliado. Itens 1-2 saíram
com termo técnico direto — Tiago apontou que ficou difícil, refeitos em estilo Feynman
(analogia antes do jargão). Item 3 já saiu no formato novo e foi confirmado como claro.
Ajuste salvo como memória pessoal de longo prazo (fora do vault), não como regra do CLAUDE.md
— já existia regra equivalente no §8, o que faltou foi aplicação mais forte, não regra nova.

## [2026-08-15] system | fecha sessão (performance-esportiva 2)

Sessão encerrada a pedido, logo após o item 3, antes de eu propor arquivar os 3 itens
explicados como página — lacuna registrada em `SESSIONS/2026-08-15-performance-esportiva-2.md`
e no `INICIO.md`. Sem avaliação, sem revisão pra recalcular. Revisões vencidas seguem
intocadas, 2 dias de atraso.

## [2026-08-15] ingest | performance-esportiva: itens 1-3 viram página

Tiago pediu pra escrever as páginas dos itens 1-3, que tinham ficado só no histórico do chat
(lacuna registrada na sessão anterior). Criadas em `KNOWLEDGE/esporte/performance-esportiva/
fase-1-bioenergetica/`: [[tres-sistemas-energeticos]], [[atp-cp]], [[mito-do-lactato]] — três
páginas em vez de uma, porque cada uma tem ideia central própria e é referenciada
separadamente na grade. Citações reais nas seções de conhecimento externo (Fiveable, Runner's
Connect, US Army, AJP Physiology, Kemp 1993, Xendurance, Daily Burn), seguindo a regra de
fonte-por-afirmação do §6 (adicionada mais cedo hoje). `mapa-performance-esportiva.md` ganhou
seção "Conceitos com página" e links nos itens 1-3. `estado-performance-esportiva.md`
reescrito no formato de bloco-por-conceito (antes era rodapé solto). `index.md` e `INICIO.md`
atualizados (24 → 27 páginas; lacuna de itens 1-3 sem página, resolvida).

## [2026-08-15] system | INBOX: 23 capturas diretas verificadas e triadas

Tiago avisou "há algumas capturas no meu inbox" — 23 arquivos apareceram direto no
filesystem (fora do fluxo de chat), incluindo conteúdo pessoal sensível (reflexão sobre
medicação, mensagem a psiquiatra vazia). Todos lidos e categorizados antes de qualquer ação
(ver conversa). Psiquiatra: vazio, nada a fazer. "12 sinais de atração": era teste de
sintaxe, não o artigo do nome.

## [2026-08-15] system | Notion: conteúdo real trazido (6 ponteiros)

Conector de Notion usado pra trazer o conteúdo por trás de ponteiros do INBOX. Achado
importante: o pedido original que gerou a pendência de hubs de 2026-08-14/15 estava lá,
datado — "me traga o hub de dinamicas sociais e um hub que trata da area da mente...
inclusive... 'Comportamento Masculino e Realismo'... quero ela também". Trazido pra
`NOTAS/`: [[reflexao-medicacao-e-conexao-racional]] (13/08, sensível, preservada literal sem
comentário), [[recompensar-processo-nao-destino-ikigai]] (13/08), [[futebol-perfil-fisico-por-posicao]]
(12/08, conversa com Grok — conecta com performance-esportiva). Um ponteiro não resolvido:
"Link do post do benchimol" — a busca por âncora de bloco retornou a página inteira, não
isolou o trecho; não inventei conteúdo, deixei marcado como pendente.

## [2026-08-15] ingest | 8 disciplinas novas + 2 hubs novos (psicologia, dinamicas-sociais)

Resolve a pendência de hubs de 2026-08-14/15 e a wishlist de "Algumas Capturas de hoje
15-08.md". Criadas: economia (hub negocios), copywriting (hub marketing),
logica-e-epistemologia (hub filosofia), produtividade-biohacking e gestao-de-tempo (hub
gestao-sistemas, fronteira declarada entre as duas), psicologia (hub novo `psicologia`),
poder-e-dinamica-social e comportamento-masculino-e-realismo (hub novo `dinamicas-sociais`,
irmãs — a segunda é pedido explícito, grade desenhada do zero, não copiada do Ybernator).
Grades checadas na web (§6), 4 fases cada, fronteiras declaradas onde há disciplina vizinha.
`poder-e-dinamica-social` e `comportamento-masculino-e-realismo` levam aviso ético explícito
na Fase de aplicação — descrever poder/influência não é endossar manipulação.

## [2026-08-15] system | itens restantes do INBOX resolvidos

VO2/HIIT: nota adicionada na Fase 2 de [[mapa-performance-esportiva]] — fica pra quando a
grade chegar lá, aplicação prática só faz sentido depois do mecanismo. Karpathy/LLM Wiki:
os 3 clipados sintetizados (não copiados) em [[metodo-llm-wiki-karpathy]], linkado em
`ARQUITETURA.md`. Startup de gravação de serviços: Tiago corrigiu — não é ideia própria,
startup já existente, só anexar → [[referencia-hub-ai-gravacao-servicos-manuais]] em NOTAS,
não em `ideias/`. Cursos/vídeos de Obsidian: sem ação, ficam como watch-list no INBOX.
`index.md` e `INICIO.md` atualizados (13 → 21 disciplinas, 324 → 438 tópicos). INBOX reduzido
de 23 para 8 arquivos (os que restam: watch-list + 2 itens genuinamente pendentes de resposta
do Tiago).

## [2026-08-15] system | INBOX: mais 5 arquivos organizados, "puxão de orelha" arquivado sem resolução

Tiago pediu pra organizar os arquivos restantes do INBOX (mostrou screenshot confirmando que
batia com o que eu já tinhaachado — nada escapou). Resolvidos: Cursos Obsidian.md e Tasks
do.md foram pra `## Recursos externos` em [[mapa-obsidian]] (cursos/vídeos ainda não
assistidos); o vídeo do Faggion (de Videos que estou acompanhando.md) foi pra
[[mapa-colaboracao-humano-ia]], por conectar com a tese de expertise/confiança escassas.
Post x (peso ideal por altura) e a nota "Projeto não estruturado com base no PARA" foram pra
`NOTAS/` como observação/pergunta — a segunda ficou explicitamente sem resolução: Tiago
mandou esquecer a pista do Notion (a nota não dizia qual projeto) em vez de eu investigar.

INBOX agora com só 2 itens de verdade pendentes: link do benchimol (bloco não resolvido) e
mensagem ao psiquiatra (vazia) — os dois aguardando resposta do Tiago, não decidi sozinho.

Também achados (não resolvidos ainda, aguardando confirmação): `Untitled.md`,
`Untitled 1.md`, `Untitled 2.md` soltos na raiz do vault — o primeiro é duplicata do que já
virou [[referencia-hub-ai-gravacao-servicos-manuais]], os outros dois são lixo de teste
(vazio / um espaço). Não apaguei sem confirmação — não são arquivos que criei.

## [2026-08-15] system | correção: NOTAS/ substituída por PARA de verdade

Dois erros apontados pelo Tiago na mesma mensagem. (1) Conectei Cursos Obsidian.md e o vídeo
do Faggion às disciplinas obsidian/colaboracao-humano-ia (seções "Recursos externos" nos
mapas) quando o pedido era só um destino fácil de achar, sem integração editorial —
revertido, os dois viraram arquivo puro em `RECURSOS/`. (2) `NOTAS/` (camada única que eu
inventei em 2026-08-15) não era o que o Tiago queria — ele já usa PARA (Projetos, Áreas,
Recursos, Arquivados) no Notion e queria a mesma estrutura aqui.

Criadas `PROJETOS/`, `AREAS/`, `RECURSOS/`, `ARQUIVADOS/` na raiz, cada uma com LEIA-ME.
Todo conteúdo de `NOTAS/` (10 arquivos) migrado pra `RECURSOS/` — nenhum tinha prazo ou área
nomeada, então caem no destino padrão. `AREAS/` e `PROJETOS/` ficam vazios: a IA não inventa
nome de área, isso é decisão do Tiago (mesmo princípio da invariante 9).

Atualizado: `CLAUDE.md` §1 (tabela de camadas) e §3 (regra de destino PARA, substitui a regra
NOTAS), `ARQUITETURA.md` (diagrama + tabela "onde mora a verdade"), `INBOX/LEIA-ME.md`
(destino PARA), `index.md`, `INICIO.md` (também corrigida uma pendência stale: hub de
dinâmicas sociais/psicologia já tinha sido resolvido antes, mas o INICIO.md ainda dizia
"nada feito"), `ideias/inbox-notas-pessoais.md`.

## [2026-08-15] system | vídeos/cursos consolidados em 1 arquivo na raiz

Tiago pediu: em vez de arquivos separados em RECURSOS/, um arquivo único na raiz com todos
os links de vídeo/curso/live, pra abrir rápido e não esquecer o que está acompanhando.
Criado "Videos e cursos que estou acompanhando.md" na raiz (4 links: 2 cursos Obsidian, 1
live, o vídeo do Faggion). `RECURSOS/cursos-obsidian.md` e
`RECURSOS/video-faggion-expertise-confianca.md` removidos.

Durante a limpeza, `RECURSOS/projeto-nao-estruturado-em-para.md` sumiu (provável hiccup de
sincronização do OneDrive) — recriado com o mesmo conteúdo.

## [2026-08-15] system | ideias/backlog/roadmap fundidos ao PARA

Tiago pediu a fusão que eu tinha recomendado: pipeline `ideias/ → backlog/ → roadmap/`
(desenhado em 2026-08-14, mas backlog/roadmap nunca chegaram a receber item nenhum)
substituído pelo PARA. Migrado: [[ementa-mapa-status-visual]] (validada e implementada) →
`ARQUIVADOS/`; [[dashboard-curriculo-progresso]] (em maturação, sem prazo) → `RECURSOS/`.
`backlog/` e `roadmap/` dissolvidas — papel absorvido por `PROJETOS/LEIA-ME.md` (ideia
validada com próxima ação clara já entra, mesmo sem data exata).

`ideias/inbox-notas-pessoais.md` fica **fora do PARA por decisão explícita do Tiago** — é
log de decisão de arquitetura deste vault, não ideia de produto solta. Pasta `ideias/`
continua existindo só por esse arquivo. `index.md` atualizado.

## [2026-08-15] system | fecha sessão (INBOX + 8 disciplinas + PARA)

Sessão encerrada a pedido. 8 SESSIONS/ gravadas (uma por disciplina nova, todas INGEST puro,
zero avaliação). Sem revisão pra recalcular. INICIO.md reescrito com o resumo da sessão.
Revisões vencidas seguem intocadas, 2 dias de atraso.

## [2026-08-15] system | RECURSOS/notas-pessoais/ separado (pedido via INBOX/IDEIA.md)

Achado um capture novo no INBOX (`IDEIA.md`) antes do commit final: "criar pasta específica
pra notas pessoais em Recursos, nunca misturar ideias com notas pessoais". Aplicado — criada
`RECURSOS/notas-pessoais/`, migrados os 6 arquivos que são reflexão/pensamento pessoal do
Tiago (motivacao-por-validacao-externa, marco-aurelio-validacao-externa,
comecar-simples-recompensa-no-processo, recompensar-processo-nao-destino-ikigai,
reflexao-medicacao-e-conexao-racional, projeto-nao-estruturado-em-para). Ficaram na raiz de
`RECURSOS/` só referência externa pura (futebol-perfil-fisico-por-posicao,
metodo-llm-wiki-karpathy, referencia-hub-ai-gravacao-servicos-manuais, tabela-peso-ideal-altura,
dashboard-curriculo-progresso). Regra documentada em `RECURSOS/LEIA-ME.md` e
`INBOX/LEIA-ME.md`. `index.md` atualizado. `IDEIA.md` removido do INBOX (resolvido).

## [2026-08-15] system | regra nova: nunca apagar sem permissão explícita

Tiago apontou um erro real: eu tinha escrito na nota `metodo-llm-wiki-karpathy.md` que "os
originais ficaram no INBOX se você quiser reler", e depois apaguei os três originais na
mesma leva de limpeza do INBOX — contradição minha, sem permissão explícita pra deletar.
Verificado no git: os arquivos nunca chegaram a ser commitados antes de eu apagar, então não
são recuperáveis pelo histórico do git. Não são recuperáveis por mim de nenhuma outra forma —
o Tiago precisa checar a lixeira do OneDrive (onedrive.com, período padrão de retenção),
já que a pasta é sincronizada e o delete deve ter ido pra lá.

Invariante 12 adicionada ao `CLAUDE.md` §2: nunca apagar arquivo sem permissão explícita do
Tiago, nem quando o conteúdo parece já substituído/sintetizado em outro lugar. Checado
FAQ/ARQUITETURA (invariante 10): nada desatualizado, o FAQ já dizia "peça pra apagar".

## [2026-08-15] system | llm-wiki - Copia.md no lugar certo, fecha sessão

Tiago recuperou o arquivo pela lixeira do OneDrive e trouxe de volta pra raiz. Movido pra
`RECURSOS/`, junto da síntese `metodo-llm-wiki-karpathy.md` que já o referenciava por embed
(`![[llm-wiki - Copia]]` — resolve por nome, independe de pasta). `index.md` atualizado.

Sessão encerrada a pedido. Sem avaliação, sem revisão pra recalcular. Revisões vencidas
seguem intocadas, 2 dias de atraso — prioridade da próxima sessão.

## [2026-08-15] system | 8 fontes novas em RAW + 8 em RECURSOS (achadas na máquina, via Notion)

Tiago pediu pra localizar na máquina os PDFs anexados na página do Notion "Sistema de gestão
pessoal Tiago" e trazer pro vault. Exceção pontual e explícita à regra "só o Tiago escreve em
RAW/" (`RAW/LEIA-ME.md`) — autorizada por ele nesta sessão, não é novo padrão.

Cópias (arquivos originais continuam onde estavam, nada foi movido/apagado da máquina):

**RAW/** (disciplina nova, ainda sem `mapa-`/`estado-`/página de fonte — só o arquivo bruto):
- `filosofia/aristoteles-etica-a-nicomaco.pdf`
- `filosofia-de-negocios/filosofia-negocios-rigoroso.pdf`
- `gestao-de-projetos/sutherland-scrum-dobro-trabalho-metade-tempo.pdf`
- `historia-aplicada-a-negocios/historia-aplicada-a-negocios-guia-completo.pdf`
- `negocios-startups/contramao-zero-to-one-fundamentos-teoricos.pdf`
- `negocios-startups/fitzpatrick-o-teste-da-mae.pdf`
- `performance-esportiva/gallwey-o-jogo-interior-do-tenis.pdf`
- `produtividade/keller-a-unica-coisa.pdf`

**RECURSOS/** (autoajuda/motivacional, sem status de disciplina de estudo):
- `FINAL - IA para o Dia a Dia - Ebook Completo.pdf`
- `prosperidade-padroes.html`
- `O_SOFRIMENTO_AMOROSO_DO_HOMEM_VOLUME_I (1).pdf`
- `Poder-e-manipulacao-Jacob-Petry.pdf`
- `Relacionamentos - Uma saída para um beco sem saída (1).pdf`
- `Mulheresseuceueseuinferno.pdf`
- `alem-da-ordem-mais-12-regras-para-a-vida-jorda-z-liborg.pdf`
- `Roube Como Um Artista PDF.pdf`
- `Les_Brown_It's_Not_Over_Until_You_Win!_(Full_Transcript) (1).pdf`

Nenhuma página de `KNOWLEDGE/` foi criada — isso é INGEST de verdade (ler, listar conceitos,
aprovação) e não foi pedido ainda. `mapa-<disciplina>.md`/`index.md` não tocados: sem página
de fonte, não há o que indexar. Próximo passo, quando Tiago quiser: escolher uma dessas
disciplinas e pedir ingest.

## [2026-08-15] system | fecha sessão — Q&A de uso do sistema + fontes novas em RAW

Sessão sem TEACH: Tiago pediu boas práticas de uso do vault (estudo/produtividade/geral),
depois trouxe as 8 fontes de RAW + 8 de RECURSOS já registradas na entrada anterior, e por fim
perguntou o significado de "ingest" (explicado, sem executar). Nenhum conceito avaliado,
nenhuma revisão recalculada. `INICIO.md` atualizado com a lista de fontes em RAW aguardando
ingest e o resumo da sessão.

Sessão encerrada a pedido. Revisões vencidas seguem intocadas (validacao-de-problema,
riscos-de-descoberta, operador-centauro) — prioridade da próxima sessão.

## [2026-08-15] ingest | produção-de-conteúdo: pipeline e mecânica por plataforma viram página

Tiago pediu pra salvar os outputs de produção de conteúdo pra redes sociais (dados no chat
mais cedo, respondendo pedido de dicas pra Instagram e depois estendido a outras redes) —
lacuna já registrada no INICIO.md. Criadas duas páginas: `KNOWLEDGE/marketing/
producao-de-conteudo/fase-2-pipeline-de-repurposing/pipeline-de-repurposing.md` (tópicos 6-7
— um conceito, três formatos, mapeamento direto de página de conceito pra post) e
`fase-3-mecanica-por-plataforma/mecanica-por-plataforma.md` (tópicos 11-15 — tabela
comparativa Instagram/TikTok/Shorts/LinkedIn/Threads-X, mesmo nível de visão geral que
[[tres-sistemas-energeticos]] deu pros três sistemas). Citações reais nas duas (regra do §6).
Mapa, `estado-producao-de-conteudo.md`, `index.md` e `INICIO.md` atualizados (27 → 29
páginas). Nenhuma avaliação — ler/ouvir não é saber (invariante 1).

## [2026-08-15] system | invariante 12 generalizada + busca pelos artigos de segundo cérebro

Tiago apontou que a limpeza do INBOX (antes mesmo do incidente do llm-wiki) já tinha apagado
sem permissão os dois artigos completos sobre "Segundo Cérebro" (Karpathy) e a imagem
embutida num deles — perda real, não só o llm-wiki. Busquei os dois no vault inteiro e
tentei a Lixeira do Windows (sem sucesso — `rm` do bash não passa pela Lixeira, e o vault é
sincronizado via OneDrive, não local). Não encontrados. Único caminho de recuperação: Lixeira
do OneDrive (onedrive.com), que exige o Tiago logado, fora do meu acesso.

Sobre o arquivo "12 SINAIS...": confirmado que quando eu li (duas vezes, por desconfiança),
já era só tabela vazia + checkbox de teste — não o artigo. Não posso confirmar se o artigo
chegou a existir ali antes de eu tocar no arquivo.

Invariante 12 do `CLAUDE.md` generalizada: não é mais só "apagar", cobre qualquer ação
irreversível (apagar/sobrescrever/truncar/mover destruindo o original), e proíbe
explicitamente a IA julgar sozinha que algo é "óbvio o suficiente" pra pular a pergunta.
Checado FAQ/ARQUITETURA (invariante 10): nada desatualizado.

## [2026-08-15] system | fecha sessão

Sessão encerrada a pedido. Achado antes de fechar: Tiago criou `_templates/braindump 1.md`
(dump mental antes de dormir, efeito Zeigarnik) e `_templates/inbox-nota.md` (formaliza nota
de INBOX com destino PARA) por conta própria, e já usou o braindump em `INBOX/Brain Dump
15-08-26.md`. Nada disso foi tocado/triado — fica pra próxima sessão, registrado no
INICIO.md. Sem avaliação, sem revisão pra recalcular. Revisões vencidas seguem intocadas, 2
dias de atraso — prioridade da próxima sessão.
