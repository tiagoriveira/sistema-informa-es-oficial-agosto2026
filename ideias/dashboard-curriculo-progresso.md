---
tipo: ideia
status: em_maturacao
criado: 2026-08-14
atualizado: 2026-08-14
---

# Dashboard/currículo de progresso (deploy Vercel)

**Ideia bruta:** um currículo que atualiza em tempo real com base no conhecimento validado do
LEARNER, e uma interface separada do Obsidian só pra ver progresso de forma rápida e visual.
Deploy no Vercel.

## Maturação

**2026-08-14** — as duas ideias (currículo + dashboard visual) são o mesmo projeto: view
read-only derivada do LEARNER, não dois sistemas. Currículo é uma página do dashboard.

Arquitetura provável: script lê `LEARNER/estado-*.md` → gera JSON → commit → Vercel rebuilda.
Vault continua fonte única — **não** sincronizar para um banco externo (Supabase, por
exemplo), dois donos da verdade quebraria o invariante "LEARNER manda".

O que dá valor real ao currículo: só entra `consolidado` — estado que exige acerto sem ajuda
em 2+ dias diferentes, com recuperação após 7+ dias. Isso é auditável de um jeito que
currículo nenhum é.

**Aviso honesto:** hoje (2026-08-14) só há 1 conceito `em_desenvolvimento`
([[operador-centauro]]) e o resto `nao_iniciado`. Gerado agora, o currículo vem
essencialmente vazio — é consequência do sistema rodando ao longo do tempo, não algo pra
construir antes de ter dado.

## Conectado com
[[ementa-mapa-status-visual]] — mesma fonte de dado (LEARNER), granularidade diferente
(disciplina inteira vs. tópico por tópico dentro de uma disciplina).

## Decisão
_(em aberto)_

_(Migrada de `ideias/` para `RECURSOS/` em 2026-08-15 — fusão do antigo pipeline
ideias/backlog/roadmap com o PARA. Ainda maturando, sem prazo, por isso Recursos e não
Projetos.)_
