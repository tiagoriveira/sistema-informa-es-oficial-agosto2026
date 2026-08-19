# Ybernator — arquivo de disciplinas importadas

## O que é isto

Em 2026-08-18, a pedido do Tiago, 123 disciplinas (3.221 tópicos) foram importadas em massa do
repositório `escola-tiago-oficial` (Ybernator) — extração automática das grades reais do
código-fonte (`src/lib/materias/*.ts`), convertidas para o formato de mapa deste vault.

No mesmo dia, também a pedido do Tiago, **tudo foi movido pra cá**. Motivo dele, nas palavras
dele: *"a IA que organizou os tópicos do Ybernator é burra, estou desconfiado em estudar por
que ela colocou e organizou ali."*

Uma amostra real (matemática, deep learning, vendas pra founder) checada antes do arquivamento
não confirmou "burrice" na lógica de sequência — mas confirmou que **nada disso passou pela
regra `CLAUDE.md` §6** (checagem web) nem por poda de tópico obsoleto. Achados concretos dessa
amostra:
- Matemática: ordem sólida, atemporal, só ordem de detalhe questionável (probabilidade tarde
  demais).
- Deep learning: erro real de posição (loss functions depois de CNN/RNN/Transformer, deveria
  vir com os fundamentos) + tópicos com prazo de validade curto (MoE, Mamba, RLHF são
  fronteira 2023-2025; comparação PyTorch vs TensorFlow já soa datada).
- Vendas pra founder: jornada bem montada, cita framework de autor real (Fitzpatrick,
  Rackham) — mas linha 16 cita ferramenta específica (Notion/HubSpot/Pipedrive) que envelhece.

Conclusão prática: **não é lixo, mas também não é confiável sem curadoria.** Fica arquivado até
alguém (Tiago, ou a IA quando pedido) processar disciplina por disciplina.

## Estrutura

```
ARQUIVADOS/ybernator/
├── LEIA-ME.md                    ← este arquivo
├── <hub>/
│   ├── hub-<hub>.md               ← só nos 5 hubs 100% novos (ver abaixo)
│   └── <disciplina>/
│       ├── mapa-<disciplina>.md
│       └── estado-<disciplina>.md
```

16 hubs no total: 5 inteiramente novos (`artes`, `ciencias-exatas-e-naturais`,
`ciencias-humanas`, `geopolitica`, `habilitacao-transito` — cada um com sua `hub-*.md`) e 11
que já existiam no vault e só receberam disciplinas extras (`comunicacao`, `dinamicas-sociais`,
`filosofia`, `financas`, `gestao-sistemas`, `inteligencia-artificial`, `marketing`, `negocios`,
`neurociencia`, `psicologia`, `tecnologia` — o hub em si continua ativo em `KNOWLEDGE/`, só as
disciplinas importadas foram pra cá).

**2 disciplinas não vieram para o arquivo:** `ingles` e `economia` colidiram com disciplina já
existente no vault (invariante 6, nome único) e foram puladas na importação original — o
conteúdo delas no Ybernator nunca chegou a entrar em lugar nenhum deste vault.

## Procedimento — quando o Tiago pedir pra trazer uma disciplina daqui pro sistema ativo

Isso é uma promoção de `ARQUIVADOS/` pra `KNOWLEDGE/`, não uma cópia direta. Siga nesta ordem:

1. **Localize** a disciplina em `ARQUIVADOS/ybernator/<hub>/<slug>/` (mapa + estado).
2. **Busca web** (regra `CLAUDE.md` §6) — confirme o que ainda é atual. Marque explicitamente
   o que envelheceu: nome de ferramenta específica, versão de framework, dado numérico datado,
   frase de fase em inglês.
3. **Pode o que estiver obsoleto** — remova tópico datado, não carregue peso morto pro sistema
   ativo. Está liberado a cortar tópico redundante ou raso demais pro padrão do vault.
4. **Revise a ordem** — a sequência importada é a do Ybernator, não uma sequência pedagógica
   pensada pra este vault. Ajuste onde a lógica falhar (ex.: fundamento aparecendo depois de
   aplicação, do jeito que aconteceu com "loss functions" em deep learning).
5. **Traduza qualquer nome de fase em inglês** que sobrar.
6. **Decida o hub certo** — se o hub de destino já existe em `KNOWLEDGE/`, verifique se a
   disciplina não sobrepõe uma existente (nesse caso, considere fundir em vez de duplicar,
   como já foi cogitado nesta conversa pra vendas/marketing/finanças). Se for um dos 5 hubs
   100% novos, promova a `hub-<hub>.md` junto e siga o invariante 13 (sequência pedagógica na
   entrada do hub, no `SYSTEM/index.md` e no `INICIO.md`).
7. **Mova** (não copie) o mapa curado pra `KNOWLEDGE/<hub>/<slug>/mapa-<slug>.md` e o estado
   pra `LEARNER/estado-<slug>.md`, com o zerar de `📍`/`⬜` reconferido contra a grade revisada.
8. **Atualize** `SYSTEM/index.md`, `INICIO.md` se for a disciplina ativa, e registre a operação
   em `SYSTEM/log.md` como `update`, citando que a origem foi este arquivo.
9. **Remova** a pasta correspondente daqui uma vez migrada — não deixe duplicado entre
   `ARQUIVADOS/` e `KNOWLEDGE/`.

Se o pedido for só "dá uma olhada" ou "quero saber o que tem aqui" — não promova nada, só leia
e relate. Promoção só acontece quando o Tiago pedir pra estudar aquilo de verdade.
