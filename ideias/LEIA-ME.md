# IDEIAS

**Pipeline substituído pelo PARA em 2026-08-15** (`PROJETOS/`, `AREAS/`, `RECURSOS/`,
`ARQUIVADOS/` na raiz — ver `LEIA-ME.md` de cada um). `ementa-mapa-status-visual.md` migrou
pra `ARQUIVADOS/`; `dashboard-curriculo-progresso.md` migrou pra `RECURSOS/`; `backlog/` e
`roadmap/` foram dissolvidas (o papel delas foi absorvido por `PROJETOS/`).

Esta pasta continua existindo só por `inbox-notas-pessoais.md` — deixado **fora do PARA por
decisão do Tiago**, por enquanto: é mais log de decisão de arquitetura deste vault (parecido
com `SYSTEM/ARQUITETURA.md`) do que ideia de produto solta.

---

_(Resto deste arquivo é o pipeline antigo, mantido como registro histórico — não é mais o
fluxo ativo.)_

Onde toda ideia nova entra, sem filtro, antes de qualquer avaliação. Não é lugar de decisão —
é lugar de não perder o pensamento. Separado do fluxo de estudo (`RAW`/`KNOWLEDGE`/`LEARNER`);
isso aqui é gestão de ideias/produto, não tutoria.

## Fluxo

```
ideia surge
   ↓
ideias/ .................. captura bruta, sem julgamento
   ↓
(opcional) maturação ..... você processa com a IA, ou deixa parada
   ↓                        pode conectar com outras ideias, pode amadurecer sozinha
validada?
   ├── sim → backlog/ ..... priorizada, sem data → roadmap/ quando ganha janela de tempo
   └── não → fica em ideias/ (maturando) ou vira status "descartada" (não se apaga)
```

Ordem corrigida em relação à primeira versão: `validada` → `backlog/` (priorização sem
compromisso de tempo) → `roadmap/` (sequenciado no tempo). É a convenção usual de produto —
backlog é "o que vale a pena", roadmap é "quando".

## Formato de arquivo (proposto)

`kebab-case-sem-acento.md`, único no vault.

```markdown
---
tipo: ideia
status: capturada
criado: AAAA-MM-DD
atualizado: AAAA-MM-DD
---

# <título curto>

**Ideia bruta:** como veio, 1-3 frases, sem polimento.

## Maturação
_(cada rodada de processamento entra aqui, com data — não sobrescreve a anterior)_

## Conectado com
_(links para outras ideias, se e quando aparecer conexão real — não force)_

## Decisão
_(preenchido só quando sai de "capturada": validada ou descartada, data, por quê)_
```

Vocabulário de status fechado (mesmo espírito do `LEARNER/` — nada de "70% pronta"):
`capturada` → `em_maturacao` → `validada` (arquivo migra para `roadmap/`) ou `descartada`
(fica aqui, arquivada — não se apaga ideia).

Ver `backlog/LEIA-ME.md` e `roadmap/LEIA-ME.md` para o formato proposto de cada pasta.
