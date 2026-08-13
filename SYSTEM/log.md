# LOG

Append-only. Nunca reescreva ou apague entrada antiga — só acrescente no fim.

Prefixo fixo, para permitir busca simples:

```bash
grep "^## \[" SYSTEM/log.md | tail -10
grep "^## \[" SYSTEM/log.md | grep ingest
```

Operações: `ingest` · `study` · `review` · `update` · `lint` · `system`

Ao virar o ano: renomeie para `log-2026.md` e comece um `log.md` novo.

---

## [2026-08-12] system | criação do vault

Estrutura inicial criada: RAW, KNOWLEDGE, LEARNER, SESSIONS, SYSTEM, _templates.
Constituição em `CLAUDE.md`, formatos em [[schema]], documentação em [[ARQUITETURA]] e [[FAQ]].
Nenhuma disciplina, fonte ou conceito ainda. Próximo passo: primeiro INGEST.

## [2026-08-13] system | ideias/roadmap/backlog + regras de sessão

Criadas pastas `ideias/`, `backlog/`, `roadmap/` (fluxo: captura → maturação → validada →
`backlog/` → `roadmap/`), formato proposto em cada `LEIA-ME.md`. `CLAUDE.md` ganhou modo
passivo no TEACH (§4) e regra de brevidade (§8), a pedido do Tiago.

## [2026-08-13] update | product-discovery

Arquivadas 4 páginas explicadas em modo passivo: [[validacao-de-problema]],
[[riscos-de-descoberta]], [[jobs-to-be-done]], [[continuous-discovery]], mais
[[mapa-product-discovery]]. Todas rotuladas como conhecimento externo (sem fonte em RAW/).

## [2026-08-13] study | product-discovery

Primeira sessão da disciplina (sem fontes em `RAW/`, modo exploração — ver `FAQ.md`).
Avaliado [[validacao-de-problema]]: acertou com hesitação a definição, errou a aplicação
(desenho de teste barato). Estado: nao_iniciado → em_desenvolvimento (nível 1, revisar
2026-08-14). Detalhe em `SESSIONS/2026-08-13-product-discovery.md`.

## [2026-08-13] update | product-discovery (2)

Arquivadas mais 3 páginas explicadas em modo passivo: [[mvp-e-tipos-de-experimento]],
[[outcome-vs-output]], [[dual-track-agile]]. `mapa-product-discovery.md` reordenado (7
conceitos). Regra de check-in em modo passivo ajustada no `CLAUDE.md` — só ao fim de bloco.

## [2026-08-13] system | 6 disciplinas registradas vazias

A pedido do Tiago (exceção deliberada à prática de "uma disciplina por vez"): registrados
mapa + estado vazios para gestao-conhecimento-second-brain, marketing,
visao-estrategica-negocios, fundamentos-sistemas-gestao, financas, ingles. Todas sem fontes.
Inglês recebeu nota de formato adaptado (não segue o modelo de conceito único).

## [2026-08-13] study | colaboracao-humano-ia

Disciplina nova, checada por busca na web (pedido do Tiago, evitar conceito desatualizado).
[[operador-centauro]]: nao_iniciado → em_desenvolvimento (acertou com hesitação, nível 1,
revisar 2026-08-14). Detalhe em `SESSIONS/2026-08-13-colaboracao-humano-ia.md`.

## [2026-08-13] study | product-discovery (2)

Segunda sessão do dia. [[validacao-de-problema]] segue em_desenvolvimento — errou de novo a
recuperação livre de métodos. [[riscos-de-descoberta]]: nao_iniciado → em_desenvolvimento
(evidência espontânea, nível 1, revisar 2026-08-14). Detalhe em
`SESSIONS/2026-08-13-product-discovery-2.md`.
