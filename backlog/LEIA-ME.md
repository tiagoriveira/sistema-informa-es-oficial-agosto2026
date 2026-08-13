# BACKLOG — ideias validadas, ainda sem compromisso de quando

Uma ideia chega aqui vinda de `ideias/` (status `validada`). Backlog é a lista de tudo que já
passou no crivo de "isso é um problema real" mas ainda não tem data — é priorização, não
agenda.

## Formato de arquivo (proposto)

```markdown
---
tipo: item-backlog
prioridade: media
criado: AAAA-MM-DD
atualizado: AAAA-MM-DD
origem: [[nome-da-ideia-original]]
---

# <título curto>

**O que é:** 1-3 frases.

**Por que foi validado:** referência curta ao que confirmou o problema (a evidência que
tirou a ideia de `ideias/`).

## Notas de priorização
_(o que muda a prioridade — não é score, é registro do motivo)_
```

`prioridade`: vocabulário fechado `alta` / `media` / `baixa` — não é score numérico.

Quando um item ganha janela de tempo definida (este trimestre, este mês), ele migra para
`roadmap/`.
