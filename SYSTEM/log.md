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
