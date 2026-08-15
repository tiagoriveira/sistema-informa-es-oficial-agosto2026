---
tipo: ideia
status: em_maturacao
criado: 2026-08-14
atualizado: 2026-08-14
---

# INBOX de notas pessoais no vault

**Ideia bruta:** transformar o vault também no lugar onde o Tiago joga notas pessoais soltas,
sem categoria definida ainda — anexa com o tipo da nota, e a IA organiza depois no local
dedicado.

## Maturação

**2026-08-14** — é PARA/CODE aplicado (capture → organize), que foi discutido na mesma sessão
em `gestao-conhecimento-second-brain`. Pasta `INBOX/` na raiz, joga com o tipo no nome, IA
move depois.

Cuidado: notas pessoais não podem cair dentro de `KNOWLEDGE/` — quebraria o orçamento de
leitura (§3 do CLAUDE.md) e o LINT. Precisam de camada própria, nível dos irmãos
KNOWLEDGE/LEARNER/SESSIONS.

Vocabulário de tipos de nota ainda não definido — decisão do Tiago, não da IA (invariante 9).

**2026-08-15** — Tiago chegou com a primeira nota pessoal na mão ("como e onde eu salvo").
Implementado o mínimo viável em vez de esperar a decisão completa: pasta `INBOX/` na raiz,
irmã de KNOWLEDGE/LEARNER/SESSIONS, com `INBOX/LEIA-ME.md` definindo o que entra, o que não
entra, e a regra de preservar o texto original literal.

## Decisão

**Parcial.** A camada existe e está em uso (3 arquivos, 2026-08-15).

**2026-08-15 (2)** — vocabulário decidido: campo `categoria:` no frontmatter, fechado em
`ideia` / `pergunta` / `observacao` / `citacao`. `tipo: nota-pessoal` continua sendo o campo
estrutural (mesmo papel que `tipo` tem em conceito/fonte/mapa/estado); `categoria` é a
natureza do conteúdo. Ver `INBOX/LEIA-ME.md`.

**2026-08-15 (3)** — Tiago apontou que `INBOX/` sozinho não bastava: nota pessoal ficava
empilhada lá sem destino final, exatamente o anti-padrão que [[nota-efemera-vs-permanente]]
descreve ("inbox" como arquivo morto com nome bonito). Criada `NOTAS/` — camada irmã, destino
permanente de nota triada que não vira KNOWLEDGE. As duas notas existentes migradas.

**2026-08-15 (4)** — `NOTAS/` **substituída por PARA de verdade**: Tiago corrigiu que o
destino devia seguir a estrutura PARA (Projetos/Áreas/Recursos/Arquivados), igual ao que ele
já usa no Notion, não uma camada única inventada. Criadas `PROJETOS/`, `AREAS/`, `RECURSOS/`,
`ARQUIVADOS/` — todo conteúdo de `NOTAS/` migrado pra `RECURSOS/` (nenhum tinha prazo/área
definida ainda). `AREAS/` e `PROJETOS/` ficam vazios até o Tiago nomear algo — a IA não
inventa área. Ver `RECURSOS/LEIA-ME.md`, `AREAS/LEIA-ME.md`, `PROJETOS/LEIA-ME.md`,
`ARQUIVADOS/LEIA-ME.md`.

Continua em aberto, e é decisão do Tiago (invariante 9):
- **nome no arquivo vs. frontmatter** — a ideia original era "joga com o tipo no nome". Ficou
  no frontmatter. Reversível.
- **quando a IA tria sozinha** — hoje não tria: marca `triada: nao` e espera. Se isso virar
  fila que não anda, o LINT precisa passar a reclamar.
- **nomear as primeiras Áreas** — `AREAS/` está vazio; sem nome definido, tudo cai em
  `RECURSOS/` por padrão.
