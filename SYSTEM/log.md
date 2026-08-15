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

## [2026-08-14] system | neurociencia-esportiva registrada

Nova disciplina, a pedido do Tiago. Mapa + estado vazios inicialmente, sem fontes ainda.
Aproveitado o momento para corrigir `SYSTEM/index.md`: filosofia estava listada como "sem
sessão" dentro de "Outras disciplinas", desatualizado desde que ganhou 9 conceitos —
promovida a seção própria, igual product-discovery.

## [2026-08-14] system | trilha em partes (agrupamento tipo Ybernator)

Inspirado na hierarquia de categorias do Ybernator (>3 sub-áreas → agrupa). "Ordem de estudo
sugerida" com mais de ~5-6 itens agora agrupa em `### Parte N — tema`, numeração corrida
(regra do ⚠️/📍 inalterada). Documentado em `schema.md` §3. Aplicado em
`mapa-neurociencia-esportiva.md` (3 partes) e `mapa-filosofia.md` (2 partes: pré-socráticos /
virada antropológica).
_(Superado no mesmo dia — ver "grade curricular" abaixo: "Parte" virou "Fase", e o
agrupamento que eu tinha inventado tinha fases de 2 itens.)_

## [2026-08-14] system | reestruturação: hub → disciplina → fase

Pedido do Tiago, inspirado na estrutura real do Ybernator (`EmentaFase {nome, topicos[]}` e
hubs com `isCategory`). KNOWLEDGE saiu de plano para 3 níveis:
`KNOWLEDGE/<hub>/<disciplina>/fase-N-<slug>/`, com o mapa sozinho no nível da disciplina.
8 hubs criados; `filosofia` virou `historia-da-filosofia` dentro do hub `filosofia` (é uma
das várias disciplinas de filosofia possíveis). `estado-filosofia.md` renomeado junto, e
todas as referências aos nomes antigos (mapa e estado) atualizadas. Links não
quebraram (invariante 6 — Obsidian resolve por nome, não por caminho). `ARQUITETURA` #8
reescrita: registrava KNOWLEDGE plano como decisão deliberada, agora registra a mudança e
por que a razão original enfraqueceu. `schema.md` §0 ganhou a árvore de pastas.

## [2026-08-14] system | grade curricular nas 10 disciplinas

Tiago recusou importar as ementas do Ybernator ("a sequência ali talvez não seja a correta e
muitos tópicos podem ter ficado obsoletos") — grades desenhadas do zero. Formato: `### Fase N
— <tema>`, 4-6 tópicos por fase, 3-6 fases, tópico descritivo em vez de nome solto de
conceito (`schema.md` §3). Total: 253 tópicos em 10 disciplinas.

Busca web (regra §6) nas que envelhecem: neurociência esportiva, colaboração humano-IA,
marketing, gestão do conhecimento, finanças, sistemas/gestão — fontes citadas em `## Nota
sobre a grade` no fim de cada mapa. Sem busca em história da filosofia (canônica), inglês
(CEFR é padrão estável) e visão estratégica (arcabouço estável, só exemplos envelhecem).
Product-discovery redesenhada sobre os 7 conceitos existentes: o buraco era método de coleta
de evidência, que virou a Fase 3.

`fundamentos-sistemas-gestao` ficou como uma disciplina só: o corte que o Tiago levantou
(sistêmico / sistemas de informação / pessoas) virou Fases 1-2, 4 e 5 — a ordem importa,
ERP sem processo é apertar botão. `financas` idem: pessoal (Fases 1-3) → corporativo (4-5).

## [2026-08-14] study | neurociencia-esportiva

Pergunta do Tiago sobre "O Jogo Interior do Tênis" (Gallwey) puxou os itens 14 e 20 da grade
antes da ordem (desvio válido pelo §4.2 — motivo: pergunta espontânea conectando os dois).
Checado na web: hipótese da ação restrita (Wulf) e teoria do reinvestimento (Masters) dão
mecanismo científico ao que o livro descreve por metáfora (Self 1/Self 2). Páginas criadas:
[[foco-atencional-nideffer]] (fase-3) e [[choking-sob-pressao]] (fase-4) — explicadas, ainda
`nao_iniciado` no LEARNER, nada testado. Gallwey citado como fonte do método, não fonte
científica — livro ainda não está em `RAW/`.

## [2026-08-14] system | fecha a sessão

`SESSIONS/2026-08-14-filosofia.md` renomeada para `2026-08-14-historia-da-filosofia.md`
(acompanha o rename da disciplina) e completada com o que aconteceu depois do primeiro
fechamento (reestruturação em hub/fase, grade de 9→33 tópicos). Criada
`SESSIONS/2026-08-14-neurociencia-esportiva.md`. Nenhuma avaliação nova em nenhuma das duas
— só explicação e reorganização; `INICIO.md` reescrito.

## [2026-08-15] system | teto de tamanho revogado

Tiago achou os itens rasos demais pra conteúdo teórico ("nos livros cada item é bem
explicado, não mastigado"). §8 do CLAUDE.md: teto de ~120/250 palavras revogado, cada
conceito agora é explicado a fundo (mecanismo, exemplo, nuance, contraponto), sem limite
fixo. §4 item 3 ajustado pra não contradizer ("profundidade vem de iterar" → "profundidade
vem do conceito bem explicado"). Ritmo de um conceito por vez continua igual — mudou
profundidade, não quantidade. Checado FAQ/ARQUITETURA (invariante 10): nada desatualizado.

## [2026-08-15] system | entrega fatiada em partes

Ajuste no mesmo dia: bloco único longo (o item 3 de gestão-conhecimento saiu inteiro —
mecanismo, exemplo, nuance, contraponto — de uma vez) também gerou fricção de leitura. §4
item 3 e §8: quanto explico (sem teto) e quanto entrego por output (uma parte do conceito por
vez — mecanismo, depois exemplo, depois nuance) são regras separadas agora.

## [2026-08-15] system | disciplina nova: obsidian

Tiago pediu "um curso sobre obsidian". Criada a 11ª disciplina, no hub `gestao-sistemas`:
`KNOWLEDGE/gestao-sistemas/obsidian/mapa-obsidian.md` (grade de 5 fases / 26 tópicos) e
`LEARNER/estado-obsidian.md` vazio. Grade checada por busca na web (§6) porque o Obsidian
mudou entre 2025 e 2026: Bases virou core plugin e assume o lugar do Dataview como caminho
padrão de dashboard; app gratuito inclusive para uso comercial. Fronteira declarada no mapa:
ferramenta aqui, método em [[mapa-gestao-conhecimento-second-brain]]. `index.md` e
`INICIO.md` atualizados (10 → 11 disciplinas, 253 → 279 tópicos).

## [2026-08-15] system | obsidian: tópico de comandos/hotkeys

Tiago pediu "comandos para produtividade no Obsidian". Entregue na conversa (paleta `Ctrl+P`
como porta única + atalhos padrão do Windows, checados na doc oficial). Grade de
[[mapa-obsidian]] passou de 26 → 27 tópicos: novo tópico 6 na Fase 1 (command palette e
hotkeys), renumerando os seguintes — a fase pulava do modelo mental direto pra links sem
passar por como se opera a ferramenta. `index.md` e `INICIO.md` acertados.

## [2026-08-15] system | página: comandos-e-hotkeys-obsidian

Tiago pediu pra salvar os comandos no vault mesmo depois de eu recomendar o contrário
(cheatsheet envelhece e a doc oficial já é referência viva). Decisão dele, página criada:
`KNOWLEDGE/gestao-sistemas/obsidian/fase-1-modelo-mental/comandos-e-hotkeys-obsidian.md`,
marcada como 100% conhecimento externo e datada 2026-08-15, com aviso de que em conflito o
app vence. Primeira página da disciplina; tópico 6 do mapa virou link. `estado-obsidian.md`
recebeu o bloco como `nao_iniciado` (entregue, não testado). `index.md` atualizado.

## [2026-08-15] study | gestao-conhecimento-second-brain

Primeira sessão da disciplina. Fase 1 explicada do item 1 ao 4 (arquivo morto, CODE, captura
seletiva, nota efêmera vs. permanente — este parcial, partes 1-2). **Nenhum virou página e
nenhum foi testado** — dívida de escrita registrada no `INICIO.md`. Duas correções de regra
no meio: teto de palavras revogado, depois entrega fatiada em partes (entradas acima).
Pedido interrompido no fim (hubs de dinâmicas sociais e mente + disciplina "Comportamento
Masculino e Realismo") — nada feito, anotado como pendente. Sessão em
`SESSIONS/2026-08-15-gestao-conhecimento-second-brain.md`.

## [2026-08-15] system | correção de data

As duas entradas de regra acima estavam datadas 2026-08-14; a sessão virou a meia-noite e o
trabalho é de 2026-08-15. Corrigidas aqui e no `CLAUDE.md` §8. Os commits de 08-14 estão
certos — aquela parte da sessão foi mesmo no dia 14.

## [2026-08-15] update | gestao-conhecimento + marcador 📖

Os 4 itens da Fase 1 viraram página: [[arquivo-morto]], [[ciclo-code]],
[[captura-seletiva]], [[nota-efemera-vs-permanente]] — todas `nao_iniciado`, só explicadas.
Pendência de escrita da sessão anterior resolvida.

Tiago perguntou por que aqui não existe o marcador de concluído que o Ybernator tem. Buraco
real: `⬜` não distinguia "nunca tocado" de "já expliquei, você só não foi testado". Criado
`📖` (explicado, nunca testado) em `schema.md` §3 — não pode ser `✅` porque ✅ aqui exige
evidência de 2+ dias, e marcar concluído só por ter sido explicado seria domínio fantasma
(invariantes 1 e 2). Legenda dos 5 símbolos adicionada ao `INICIO.md`.
