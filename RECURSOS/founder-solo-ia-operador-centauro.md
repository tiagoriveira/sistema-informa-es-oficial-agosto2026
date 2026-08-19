---
tipo: nota-pessoal
categoria: referencia-externa
autor: tiago
criado: 2026-08-19
origem: notion (fundida) + revisão web
triada: sim
---

# Founder solo com IA — sistema operacional pessoal (Operador Centauro)

> Fusão de duas notas do Notion do Tiago ("NOTA IA CLAUDE COMO FOUNDER SOLO EM 2026",
> capturada 2026-06-14, e "NOTA GPT FOUNDER SOLO - OPERADOR CENTAURO", capturada 2026-06-12,
> que se linkavam entre si no Notion original). Fundidas e atualizadas em 2026-08-19 a pedido
> do Tiago ("funda em apenas um, aprimorando o doc e deixando consistente com práticas
> atualizadas") — checado contra busca na web (regra `CLAUDE.md` §6), não só memória de
> treino. O que veio das notas originais e o que foi corrigido/atualizado nesta revisão está
> marcado separadamente na seção final, pra não misturar silenciosamente.

## Premissa
Founder solo (consultoria + produto digital, ou qualquer operação sozinha com múltiplos
projetos): o problema central não é falta de ferramenta, é **troca de contexto** — o cérebro
não executa várias tarefas complexas em paralelo, só alterna entre elas, e cada alternância
tem custo cognitivo. A filosofia do **Operador Centauro** (humano + IA) é aceitar essa
limitação e transformar a IA em extensão operacional da memória, análise e execução — mesmo
termo já usado neste vault em [[operador-centauro]] (humano planeja/decide, IA executa).

## 1. Um sistema central, não um por projeto
Regra original: tudo entra no mesmo sistema (um gerenciador de tarefa, um banco de
conhecimento, um dashboard), separado por área/projeto — nunca WhatsApp pra um projeto,
Notion pra outro, papel pra outro. Isso continua válido e é, hoje, prática consolidada
("single source of truth"): a atualização de 2026 é que esse sistema central passou a incluir
uma **camada de memória tratada como componente arquitetural separado**, não só um repositório
de arquivo — a IA lê esse repositório (Obsidian, Notion ou RAG próprio) pra ter contexto do
negócio entre sessões, e escreve nele de volta.

## 2. IA como memória persistente — modelo atualizado
As notas originais propunham **um GPT dedicado por projeto** (ex.: GPT Marketing, GPT
E-commerce), cada um guardando objetivo/contexto/histórico/documento próprio. Isso já foi a
prática de 2026-06; a prática de 2026-08 convergiu pra outro desenho: em vez de vários agentes
isolados com memória própria, o padrão que virou default é **um orquestrador central com
memória compartilhada e acesso por escopo** — a memória fica numa camada única (arquivo de
projeto/log append-only, ou banco vetorial), e cada tarefa recupera só o que é relevante por
similaridade semântica antes de agir. Reduz duplicação de contexto e evita que os "GPTs"
percam sincronia entre si. Pra founder solo especificamente, o orquestrador centralizado
(coordenador único com estado global) costuma ser a escolha certa — reduz a complexidade de
estado distribuído que só compensa em equipe.

## 3. Operar por ciclo / estágio, não por dia solto
- **Ciclos temáticos**: agrupar atividade semelhante (ciclo estratégico, comercial,
  operacional) em vez de fazer tudo todo dia — reduz custo de troca de contexto.
- **Dias temáticos**: dia fixo por foco (crescimento/vendas, produto, conteúdo, estratégia,
  revisão/sistema).
- **Separar projeto por estágio, não por tema**: Exploração / Construção / Escala /
  Manutenção — cada estágio pede tipo de atenção diferente.
- **Regra dos 3 níveis**: no máximo 1 projeto principal (70% do tempo), 1 secundário (20%), 1
  experimental (10%) simultâneos.

## 4. Divisão de trabalho — Operador Centauro
**Humano:** decisão, julgamento, criatividade, negociação, trade-off, risco.
**IA:** pesquisa, resumo, organização, documentação, primeiro rascunho, análise de dado,
tarefa repetitiva (3+ vezes/semana vira candidata a automação).
Regra citada nas notas originais: "nunca faça manualmente algo que a IA consiga fazer com 80%
da qualidade em menos de 2 minutos." Em 2026-08, o operador de alta performance se comporta
mais como **gestor de agente e processo** do que como executor — quanto mais projeto, menos
importa a capacidade de fazer tarefa e mais importa a capacidade de orquestrar agente,
automação e prioridade.

## 5. Revisão e priorização
- **Revisão semanal obrigatória** (proposta: domingo): o que avançou, o que travou, o que
  pode ser automatizado, o que deveria ser eliminado. Eliminar é tão importante quanto
  executar.
- **Dashboard de 3 listas**: Crescimento (gera mais valor) / Manutenção (mantém funcionando) /
  Eliminação (deveria parar).
- **Métrica de alavancagem por atividade**: 1x (resolver problema operacional) → 10x (criar
  processo) → 100x (automatizar processo) → 1000x (construir ativo que gera resultado sem
  presença). Priorizar sempre a de maior multiplicação.
- **Estrutura sugerida**: até 5 projetos ativos, só 3 recebendo atenção real, 1 prioridade
  dominante por trimestre.

## 6. Ikigai como filtro operacional (não só reflexão anual)
Founder solo é o próprio ativo principal — sem equipe pra absorver trabalho sem sentido, o
burnout chega rápido mesmo com sistema perfeito. Os 4 círculos (versão ocidental do Ikigai,
atribuída a Marc Winn 2014 — não é a origem japonesa tradicional) viram critério operacional:
- **Ama fazer** — rastreio semanal de energia por tarefa; o que drena por muito tempo vira
  candidato a delegar.
- **É bom nisso** — força única real (facilidade desproporcional, não só competência); cada
  projeto marca se exige essa força ou é automatizável/terceirizável.
- **Mundo precisa** — Jobs To Be Done emocional: qual transformação real o cliente recebe.
- **Pagam por isso** — filtro de cliente: aceitar só quem se beneficia do que você
  genuinamente faz bem; cliente que paga bem mas quebra os outros 3 círculos, declinar.
- **Ritual trimestral**: trabalhei no que amo ou no que drena? / sou contratado pelo que sou
  bom ou pelo que consigo fazer? / cliente precisa de verdade ou é conveniência mútua? / o
  dinheiro vem de onde dói menos ou de onde importa mais?

## Frameworks citados (todos conceito público, não proprietários das notas originais)
BHAG (Collins), OODA Loop (Boyd), matriz de Eisenhower, GTD (Allen), PARA (Forte), Jobs To Be
Done (Christensen), Zettelkasten light (Luhmann), Profit First (Michalowicz), Ikigai (versão
ocidental, Marc Winn).

## O que foi atualizado nesta revisão (2026-08-19)
- **Seção 2 reescrita**: "um GPT por projeto" (nota original) → orquestrador central com
  memória em camada única e recuperação por escopo/similaridade semântica — é o padrão que se
  consolidou entre jun/2026 e ago/2026, e reduz a fragmentação que a própria filosofia das
  notas originais queria evitar.
- **Seção 1 complementada**: memória agora tratada como "componente arquitetural separado",
  não só arquivo — reflete prática de 2026-08, não estava nas notas originais.
- Nada foi removido — só complementado. Ver [[mapa-arquitetura-de-agentes-e-contexto]] pra
  aprofundar essa camada técnica além do resumo aqui.

## Ressalvas que permanecem (das notas originais, ainda não verificadas)
- Números de meta (ex.: R$ 50k/mês, 4h/dia, 70% autônomo, citados na nota Claude original) são
  arbitrários, sem benchmark verificável.
- "Queima em 18 meses" (risco de burnout do founder solo) é observação qualitativa de
  comunidade, não dado científico.
- Nenhuma das duas notas nem esta revisão substitui conversa real com cliente/mercado —
  continua brainstorm estruturado, não autoridade.

**Fontes da revisão de 2026-08-19:**
- [State of AI Agent Memory 2026 — Mem0](https://mem0.ai/blog/state-of-ai-agent-memory-2026)
- [One-Person Company Software: The Solo AI Tool Stack (2026) — Taskade](https://www.taskade.com/blog/one-person-companies)
- [Effective context engineering for AI agents — Anthropic](https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents)
