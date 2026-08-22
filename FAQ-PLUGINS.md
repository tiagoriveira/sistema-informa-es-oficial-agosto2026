# FAQ — Plugins do Obsidian

Uso prático dos plugins instalados neste vault. Regras do sistema de estudo: `CLAUDE.md`.
Decisões de arquitetura (inclusive o que **não** foi instalado e por quê): `SYSTEM/ARQUITETURA.md`.

Instalados em 2026-08-22, verificados em `.obsidian/community-plugins.json`:
`obsidian-spaced-repetition`, `flashcards-obsidian`, `quickadd`, `nldates-obsidian`,
`templater-obsidian`, `tag-wrangler`.

---

## Spaced Repetition

**Pra quê:** flashcards com repetição espaçada, rodando dentro do Obsidian — hoje usado
principalmente pra vocabulário/frase de inglês (ver [[mapa-ingles]] e
[[Como usar Spaced Repetition para aprender inglês]]), mas serve pra qualquer disciplina que
precise de recall de volume alto (fato solto, data, fórmula) em vez de conceito explicado.

**Como revisar:** paleta de comando (`Ctrl/Cmd+P`) → "Review flashcards", ou o ícone de cartão
na barra lateral esquerda.

**Como criar cartão:** dentro de qualquer nota com a tag `#flashcards` (padrão do plugin) —
```
Pergunta::Resposta                    → cartão de linha única
Pergunta:::Resposta                   → cartão reverso (gera nos dois sentidos)
Pergunta
?
Resposta                              → cartão multi-linha
Frase com ==palavra-chave== oculta.   → cloze (lacuna)
```

**Não substitui o LEARNER.** Conceito de disciplina (gramática, framework, o que for) continua
sendo ensinado e avaliado por mim, em conversa — o plugin é só pra volume alto de fato atômico.
Ver a tabela de divisão em [[Como usar Spaced Repetition para aprender inglês]].

⚠️ **Também está instalado `flashcards-obsidian`** (plugin diferente, não recomendado por mim —
apareceu instalado quando chequei `.obsidian/plugins/`). Os dois fazem flashcard de formas
distintas e podem conflitar ou duplicar cartão se usados ao mesmo tempo sem cuidado. Não decidi
por você — se notar comportamento estranho na revisão (cartão duplicado, sintaxe não
reconhecida), provavelmente é os dois brigando pelo mesmo texto. Considere desativar um dos
dois em Configurações → Community plugins.

---

## Templater

**Pra quê:** usar os templates de `_templates/` (`mapa.md`, `conceito.md`, `sessao.md`,
`estado-disciplina.md`, `fonte.md`) direto ao criar nota nova, sem copiar e colar — já previsto
em `SYSTEM/ARQUITETURA.md` (mudança menor #22).

**Como usar:** Configurações → Templater → aponte a pasta de templates pra `_templates/`. Depois,
ao criar nota nova: paleta de comando → "Templater: Insert Template", escolhe o template.

---

## Tag Wrangler

**Pra quê:** renomear ou mesclar tag em massa no vault inteiro — útil agora que existe o padrão
`#taskia`, `#taskia1`, `#taskia2`... no [[TAREFAS]]. Se o padrão de tag mudar (por exemplo,
decidir renomear `#taskia` pra outra coisa), Tag Wrangler evita ter que editar arquivo por
arquivo à mão.

**Como usar:** passe o mouse sobre qualquer tag no painel de tags (barra lateral direita) →
botão direito → "Rename tag" ou "Merge tag".

---

## QuickAdd

**Pra quê:** capturar rápido de qualquer lugar do Obsidian (ou até fora dele, com atalho de
sistema) direto pra seção "Captura rápida" do [[TAREFAS]], sem precisar abrir o arquivo primeiro
— é a ferramenta que faz a promessa do `#taskia2` (ver `TAREFAS.md`, "Feito recentemente")
funcionar sem fricção.

**Como configurar:** Configurações → QuickAdd → "Add Choice" → tipo "Capture" → aponta o destino
pra `TAREFAS.md`, seção "Captura rápida" (usa a opção de inserir sob um cabeçalho específico).
Depois define um atalho de teclado pra esse Choice em Configurações → Hotkeys.

---

## Natural Language Dates

**Pra quê:** digitar "hoje", "amanhã", "semana que vem" e o plugin converte pro formato
`AAAA-MM-DD` que o `CLAUDE.md` exige em todo frontmatter (`schema.md` §0) — evita erro de
formato de data feito à mão.

**Como usar:** digite a data em linguagem natural e use o comando "Natural Language Dates:
Parse date" (paleta de comando), ou configure o autocomplete pra sugerir enquanto digita.

---

## O que não está instalado, de propósito

**Dataview** e plugin de embedding/similaridade entre notas (tipo "Open Connections") — ambos
recomendados por comentário no post do Threads (`tiagoribeiro.rs1`, 2026-08-21/22), mas **não
instalados**. Não é dogma (`CLAUDE.md` invariante 15) — é uma recomendação revisável, registrada
aqui com o raciocínio completo pra não se perder, discutida em 2026-08-22.

### Dataview, em termos simples
Dataview deixa você escrever uma **pergunta** dentro de uma nota (tipo busca de banco de dados)
e ele monta uma tabela **ao vivo**, escaneando outras notas — sem copiar e colar, atualiza
sozinha conforme o vault muda. Analogia: é a diferença entre lista de compras escrita à mão
(envelhece assim que você usa um item) e uma tela mostrando "o que tem na geladeira agora".

### Onde funcionaria hoje, sem mexer em nada
Toda página de conceito já tem frontmatter estruturado (`tipo:`, `criado:`, `fontes:`). Dataview
lê frontmatter bem — uma query real que já rodaria:
```dataview
TABLE disciplina, criado
FROM "KNOWLEDGE"
WHERE tipo = "conceito" AND fontes = []
```
Isso mostraria, ao vivo, toda página marcada como "conhecimento externo" (sem fonte sua) — útil
pra auditar rápido sem pedir pra mim.

### Onde não funcionaria, do jeito que o vault está hoje
A pergunta mais óbvia que todo mundo quer — "o que tá vencido pra revisar?" — não dá, porque
`estado`, `nível` e `revisar:` vivem em **texto corrido** dentro de cada bloco do
`LEARNER/estado-<disciplina>.md`, não em campo estruturado. Dataview não lê prosa, lê campo.
Pra essa query funcionar, cada conceito precisaria virar arquivo próprio com
`revisar:: 2026-08-25` no frontmatter — o que desfaz a mudança #1 de `ARQUITETURA.md`: quando o
LEARNER era um arquivo por conceito, as dimensões do mesmo conceito viviam espalhadas e podiam
se contradizer entre si. Reestruturar de volta troca "nunca diverge de si mesmo" por "dashboard
bonito".

### Prós e contras

**A favor:**
- Zero risco — é só visual, humano; se não gostar, para de usar, nada quebra.
- Já dá pra testar hoje em cima do que já é estruturado (`KNOWLEDGE`), sem mexer em `LEARNER`.
- Painel na hora, sem precisar perguntar pra mim.

**Contra:**
- Eu **não leio o resultado da tabela** — só o código da pergunta. Decisão tomada olhando uma
  tabela desatualizada/quebrada, e eu não saberia, porque pra mim ela nem existe.
- A query mais desejada (revisão vencida) não funciona sem reestruturar `LEARNER`.
- Campo com nome errado quebra a query em silêncio — tabela vazia, sem erro claro.

### Recomendação (não decisão)
Vale testar nas perguntas que já funcionam de graça (frontmatter de `KNOWLEDGE`), não
reestruturar `LEARNER` pra caçar a query de revisão — o custo dessa reestruturação já foi pago
uma vez e a razão pra evitar continua valendo. `ARQUITETURA.md` #12 e #13 documentam a decisão
original; esta seção é a expansão prática dela.
