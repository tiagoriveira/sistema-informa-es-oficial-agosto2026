# ROADMAP — o que está sequenciado no tempo

Um item chega aqui vindo de `backlog/`, quando ganha uma janela de tempo definida — não é mais
"algum dia", é "neste período". Roadmap é compromisso de sequência, não lista de desejos.

## Formato de arquivo (proposto)

```markdown
---
tipo: item-roadmap
periodo: "2026-Q3"
status: planejado
criado: AAAA-MM-DD
atualizado: AAAA-MM-DD
origem: [[nome-do-item-backlog]]
---

# <título curto>

**O que é:** 1-3 frases.

**Por que agora:** o que fez este item ganhar janela de tempo em vez de continuar no backlog.

## Progresso
_(atualizações curtas com data, não um changelog completo)_
```

`status`: vocabulário fechado `planejado` / `em_andamento` / `concluido` / `adiado`.
`periodo` é qualitativo (trimestre/mês), não uma data de entrega prometida.
