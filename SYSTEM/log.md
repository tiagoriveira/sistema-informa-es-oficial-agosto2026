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

## [2026-08-14] system | filosofia registrada

Nova disciplina, a pedido do Tiago (decidiu manter separada do vault-conhecimento-ia, que
segue só para notas atômicas via skill `obsidian-filosofia`). Mapa + estado vazios, sem
fontes ainda.

## [2026-08-14] study | filosofia

Primeira sessão. [[mito-para-logos]] (Tales de Mileto, virada mythos→logos): nao_iniciado →
em_desenvolvimento, acertou sem ajuda por que Tales é o primeiro filósofo (nível 2, revisar
2026-08-17). Página criada em KNOWLEDGE, rotulada como conhecimento externo (sem fonte RAW).

## [2026-08-14] update | filosofia (modo passivo)

A pedido do Tiago, TEACH passou a checar só ao fim de bloco (não a cada output) — CLAUDE.md
§4 ajustado. Depois disso, Tiago pediu modo passivo (sem pergunta nenhuma por hora).
Explicados em sequência: [[anaximandro-apeiron]], [[anaximenes-ar]],
[[heraclito-fluxo-e-logos]], [[parmenides-ser-imutavel]]. Páginas criadas, todas
`nao_iniciado` no LEARNER — nada testado ainda, conteúdo só explicado. Depois, páginas de
[[empedocles-quatro-raizes]] e [[democrito-atomismo]] também criadas, mesmo estado.

## [2026-08-14] system | protocolo de entrega reescrito (CLAUDE.md §4 e §8)

Inspirado em análise do repo Ybernator (app de estudos do Tiagolink repo: https://github.com/tiagoribeiror58-debug/escola-tiago-oficial.git ) a pedido dele. TEACH: item 3
virou "entrega de fricção zero" (explica direto, sem pergunta de abertura, exemplo/aplicação
prática, termina bloco com menu de próximos passos, não pergunta); item 4 isola avaliação em
momento próprio (só quando pedido, revisão vencida, ou modo ativo sinalizado) — substitui a
exceção "modo passivo", que virou o comportamento padrão. §8 ganhou teto numérico (~120
palavras/conceito, ~250/output) no lugar de "curto por padrão". 3 ideias maiores da mesma
conversa (dashboard/currículo, INBOX de notas, ementa com status ✅📍⬜) foram para `ideias/`
em vez do CLAUDE.md — são produto, não regra de tutor.

## [2026-08-14] update | filosofia (2)

Páginas de [[sofistas-relativismo]] e [[socrates-metodo-elenchos]] criadas (explicados em
bloco, ainda não testados) antes de fechar a sessão — conteúdo que só existia no chat.
Correção: datas de todo o trabalho de filosofia estavam erradas como 2026-08-13; corrigidas
para 2026-08-14 (data real), incluindo o revisar de [[mito-para-logos]] (2026-08-16 →
2026-08-17). Sessão fechada em `SESSIONS/2026-08-14-filosofia.md`.

## [2026-08-14] system | FAQ e ARQUITETURA desatualizados pelo protocolo novo

Tiago pediu auditoria de consistência entre FAQ.md/ARQUITETURA.md e o CLAUDE.md real.
Achados: FAQ descrevia "abre com pergunta" como padrão (virou exceção hoje), e ambos
descreviam git commit como manual (agora é automático ao encerrar). Corrigidos os dois.
CLAUDE.md ganhou invariante 10 (checar FAQ/ARQUITETURA sempre que uma regra mudar) e o passo
5 do UPDATE (git push automático, que já valia por pedido do Tiago mas só estava na memória
da IA, não no CLAUDE.md).

## [2026-08-14] system | ementa visual implementada ([[ementa-mapa-status-visual]])

Ideia validada e executada no mesmo dia. Status visual (✅⚠️📍⬜) na "Ordem de estudo
sugerida" do mapa — cache derivado do LEARNER, regenerado a cada UPDATE. Formato em
`schema.md` §3, regra no `CLAUDE.md` (UPDATE). Aplicado em `mapa-filosofia.md`: 📍 em
[[mito-para-logos]] (único avaliado), resto ⬜.

## [2026-08-14] system | auditoria semanal automática configurada

Routine na nuvem (`trig_012aX6ua3PESCJ8B5Gmq1ece`), roda todo domingo 20h BRT (23h UTC).
Audita CLAUDE.md vs FAQ/ARQUITETURA, links quebrados, páginas órfãs, conceitos sem entrada no
LEARNER, revisões vencidas, INICIO.md/index.md fora de sincronia. Só reporta (não corrige),
escreve entrada `lint` no fim deste log e dá push — sem tocar em mais nada. Removi os
conectores MCP que vieram anexados por padrão (Meta Ads, Notion, Vercel, etc.) — a auditoria
só precisa do repo git. CLAUDE.md §3 ganhou "git pull no início da sessão", senão o relatório
semanal fica preso no GitHub e a sessão local nunca vê.
