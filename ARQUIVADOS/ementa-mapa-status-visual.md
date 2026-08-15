---
tipo: ideia
status: validada
criado: 2026-08-14
atualizado: 2026-08-14
---

# Ementa com status visual (✅📍⬜) no mapa da disciplina

**Ideia bruta:** trazer pro sistema a lógica do Ybernator (app de estudos do Tiago) de mostrar
um mapa/ementa de tópicos com o que já foi concluído, o que é sugerido a seguir e o que está
disponível — pra ver de forma rápida o que falta estudar.

## Maturação

**2026-08-14** — inspirado no `mapa` do Ybernator (`✅` concluído / `📍` sugerido / `⬜`
disponível) sobre `KNOWLEDGE/<disciplina>/mapa-<disciplina>.md`.

Prós: visual instantâneo sem abrir o LEARNER inteiro; barateia a decisão de "o que estudar"
(§4.2 do CLAUDE.md); vira dado de graça pra [[dashboard-curriculo-progresso]].

Contras e como mitigar:
- **Duplica estado** (mapa + LEARNER) → precisa ser cache derivado, no espírito do
  `INICIO.md`: nunca editado à mão, sempre regenerado a partir do LEARNER quando ele muda.
- **3 símbolos não cobrem `fragil`** (regressão) → precisaria de um 4º símbolo (ex.: ⚠️) pra
  não perder essa nuance no mapa.
- **Só funciona com ordem de estudo definida** → a maioria das disciplinas ainda está em modo
  exploração, sem ordem fixa. Aplicar só onde já existe "Ordem de estudo sugerida" (caso de
  `filosofia` hoje).

Ainda falta fechar o mapeamento exato de símbolo↔estado com o Tiago antes de mexer no
`schema.md` — não é decisão da IA sozinha (invariante 9).

## Conectado com
[[dashboard-curriculo-progresso]]

## Decisão
**2026-08-14 — validada e implementada.** Mapeamento fechado: ✅ consolidado · ⚠️ fragil ou
revisão vencida (primeiro item não-✅ nessa condição) · 📍 primeiro item não-✅ fora dessa
condição (sugestão de próximo passo) · ⬜ resto. Formato em `SYSTEM/schema.md` §3, regra de
regeneração no `CLAUDE.md` (UPDATE), primeira aplicação em `mapa-historia-da-filosofia.md`.

_(Migrada de `ideias/` para `ARQUIVADOS/` em 2026-08-15 — fusão do antigo pipeline
ideias/backlog/roadmap com o PARA. Já implementada, por isso arquivada, não em RECURSOS.)_
