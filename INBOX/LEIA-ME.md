# INBOX — notas pessoais

Camada irmã de `KNOWLEDGE/`, `LEARNER/` e `SESSIONS/`. Criada em 2026-08-15.

**O que entra aqui:** pensamento seu, cru, sem categoria decidida ainda. Você joga, a IA
tria depois. Não precisa estar bem escrito nem estar "pronto".

**O que NÃO entra:** conhecimento vindo de fonte (isso é `KNOWLEDGE/`), estado de
aprendizagem (`LEARNER/`), registro de sessão (`SESSIONS/`).

**Por que camada separada e não uma pasta dentro de `KNOWLEDGE/`:** o orçamento de leitura
do `CLAUDE.md` §3 depende de `KNOWLEDGE/` conter só página destilada e citável. Nota pessoal
crua ali dentro faria a IA ler lixo achando que é fonte, e o LINT reclamaria de órfã em cada
passada.

## Regras

- Nome do arquivo: `AAAA-MM-DD-<slug-kebab-case>.md`.
- **O texto original do Tiago é preservado literal**, num bloco marcado. A IA pode acrescentar
  estrutura ao redor, nunca reescrever por cima.
- Nota do INBOX **não é fonte**. Não citar como autoridade em página de KNOWLEDGE.
- Triagem é operação separada: virar página de conceito exige aprovação (invariante 8).

## Destino, depois de triada (PARA — decidido em 2026-08-15)

`INBOX/` é efêmera — não é pra ficar aqui pra sempre ([[nota-efemera-vs-permanente]]). Depois
de triada, a nota sai daqui pro método PARA (Tiago Forte), igual à estrutura que você já usa
no Notion:

- Vira **conceito citável de uma disciplina** → `KNOWLEDGE/` (pede aprovação, invariante 8).
- Tem prazo e próxima ação clara → `PROJETOS/`.
- Responsabilidade contínua que você já nomeou → `AREAS/<nome>/` — a IA não inventa área.
- Referência sem compromisso ativo → `RECURSOS/`, destino padrão. Reflexão/pensamento
  pessoal vai em `RECURSOS/notas-pessoais/`; referência externa pura fica na raiz de
  `RECURSOS/` — nunca misturar os dois no mesmo arquivo (regra de 2026-08-15).
- Ficou inativo → `ARQUIVADOS/`.

Nenhum desses (fora KNOWLEDGE) precisa de aprovação prévia — é organização, não criação de
conteúdo novo.

## Categoria (frontmatter `categoria:`)

Vocabulário fechado, decidido em 2026-08-15:

- `ideia` — pensamento seu, interpretação
- `pergunta` — dúvida em aberto
- `observacao` — algo notado, sem elaboração
- `citacao` — trecho trazido de outra fonte
