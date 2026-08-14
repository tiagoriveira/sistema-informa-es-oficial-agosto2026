# schema — formatos de página

Referência de formato. As regras de comportamento estão em `CLAUDE.md` (constituição) — este
arquivo não repete regra, só define **como cada página é escrita**. Leia sob demanda, na hora
de escrever uma página do tipo correspondente.

---

## 0. Convenções gerais

**Nome de arquivo:** `kebab-case-sem-acento.md`. Único no vault inteiro (o `[[link]]` do
Obsidian resolve por nome de arquivo, não por caminho). Colisão entre disciplinas → sufixo:
`elasticidade-economia.md`, `elasticidade-fisica.md`.

**Título legível** vai no frontmatter (`titulo:`) e no `# H1`. O nome do arquivo pode ser feio;
o título não.

**Datas:** sempre `AAAA-MM-DD`. Nunca "ontem", "semana passada", "recentemente".

**Links:** `[[nome-do-arquivo]]`. Todo conceito cita pelo menos um vizinho — página sem link é
página órfã e o LINT vai reclamar.

**Frontmatter:** só campos que são usados de fato. Campo que ninguém lê é dívida de manutenção.

---

## 1. Página de conceito

`KNOWLEDGE/<disciplina>/<conceito>.md`

```markdown
---
tipo: conceito
disciplina: economia
titulo: Elasticidade-preço da demanda
fontes: [mankiw-cap-5]
criado: 2026-08-12
atualizado: 2026-08-12
---

# Elasticidade-preço da demanda

**Ideia central:** quanto a quantidade demandada reage a uma variação de preço.

## Explicação
Mede a variação percentual da quantidade dividida pela variação percentual do preço
(cf. [[mankiw-cap-5]], p. 90). Como preço e quantidade se movem em direções opostas, o
resultado é negativo; a convenção é trabalhar com o módulo.

- |E| > 1 → elástica: a quantidade reage mais que proporcionalmente
- |E| < 1 → inelástica: a quantidade reage menos que proporcionalmente
- |E| = 1 → unitária

## Determinantes
- existência de substitutos próximos (cf. [[mankiw-cap-5]], p. 91)
- bem essencial vs. supérfluo
- horizonte de tempo — quase tudo é mais elástico no longo prazo

## Exemplos
- Insulina: inelástica, não há substituto.
- Refrigerante de uma marca específica: elástica, o concorrente está na prateleira ao lado.

## Erros comuns
- Confundir com [[elasticidade-renda]] — aqui varia o **preço**, lá varia a **renda**.
- Ler o sinal negativo como "elasticidade baixa".

## Relacionado
[[oferta-e-demanda]] · [[elasticidade-renda]] · [[receita-total]]

## Divergências entre fontes
_(só existe se houver divergência de verdade; caso contrário, remova a seção)_

## Conhecimento externo (fora das suas fontes)
_(só existe se houver; sempre rotulado)_
```

Regras:
- **Ideia central em uma frase.** Se não couber, a página está grande demais — divida.
- Alvo de tamanho: **40–120 linhas**. Passou muito disso, provavelmente são dois conceitos.
- `## Erros comuns` é povoada tanto pela fonte quanto pelos erros reais do Tiago. Erro que ele
  cometeu de verdade entra aqui **e** no LEARNER.

---

## 2. Página de fonte

`KNOWLEDGE/<disciplina>/fontes/<fonte>.md`

Uma por unidade ingerida. Livro grande = uma página por capítulo + uma página-mãe do livro.

```markdown
---
tipo: fonte
disciplina: economia
titulo: "Mankiw — Introdução à Economia, cap. 5 (Elasticidade)"
arquivo_raw: RAW/economia/mankiw-introducao-economia.pdf
paginas: 89-108
ingerido: 2026-08-12
---

# Mankiw — cap. 5, Elasticidade

**O que esta fonte ensina:** como medir a sensibilidade de demanda e oferta a preço, renda
e preços cruzados, e por que isso determina o efeito de um choque sobre a receita.

## Conceitos extraídos
- [[elasticidade-preco]] — p. 90
- [[elasticidade-renda]] — p. 96
- [[receita-total]] — p. 98

## Pontos que a fonte enfatiza
- Insiste que o horizonte de tempo muda a resposta (p. 93). Se a fonte insiste, o tutor
  também insiste.

## Trechos-chave
> "A elasticidade-preço da demanda mede o quanto..." (p. 90)

## Não coberto por esta fonte
- Elasticidade de oferta em mercados com capacidade restrita.
```

`## Não coberto` é o que alimenta lacunas honestas: sabemos o que a fonte **não** diz.

---

## 3. Mapa da disciplina

`KNOWLEDGE/<disciplina>/mapa-<disciplina>.md` — o MOC. É por aqui que se decide o que estudar.

```markdown
---
tipo: mapa
disciplina: economia
atualizado: 2026-08-12
---

# Mapa — Economia

**Fontes desta disciplina:** [[mankiw-cap-4]] · [[mankiw-cap-5]]
**Estado do aluno:** [[estado-economia]]

## Ordem de estudo sugerida
1. [[oferta-e-demanda]] — base de tudo
2. [[elasticidade-preco]] — depende de 1
3. [[receita-total]] — depende de 2

## Conceitos por tema

### Microeconomia — mercado
- [[oferta-e-demanda]] — como preço e quantidade se equilibram
- [[elasticidade-preco]] — quanto a quantidade reage a preço

## Ainda sem página (mencionados, não desenvolvidos)
- excedente do consumidor — aparece em [[mankiw-cap-4]], sem página ainda

## Perguntas em aberto
- Como elasticidade interage com política de imposto? (não coberto pelas fontes atuais)
```

### Status visual na "Ordem de estudo sugerida"

Só se aplica quando a disciplina já tem essa seção (ordem definida). Prefixe cada item com um
símbolo — **cache derivado do LEARNER**, nunca editado à mão, regenerado toda vez que o
LEARNER daquela disciplina muda (mesmo princípio do `INICIO.md`):

- `✅` consolidado
- `⚠️` fragil, ou revisão vencida (varre a ordem; o primeiro item ainda não `✅` que estiver
  nessa condição recebe este símbolo)
- `📍` se o primeiro item ainda não `✅` **não** estiver em `⚠️`, ele recebe este símbolo —
  é a sugestão de próximo passo
- `⬜` todo o resto (nao_iniciado ou em_desenvolvimento fora do primeiro item pendente)

Exatamente um item por vez fica `⚠️` ou `📍` (o primeiro não-`✅` da lista) — não os dois.

```markdown
## Ordem de estudo sugerida
1. ✅ [[mito-para-logos]]
2. ⚠️ [[anaximandro-apeiron]]
3. ⬜ [[anaximenes-ar]]
```

---

## 4. Estado do aluno (LEARNER)

`LEARNER/estado-<disciplina>.md` — **um arquivo por disciplina**, um bloco por conceito.
Todas as dimensões do mesmo conceito ficam juntas: atualizar um conceito é editar um lugar só.

```markdown
---
tipo: estado
disciplina: economia
atualizado: 2026-08-12
---

# Estado — Economia

## [[oferta-e-demanda]]
estado: consolidado · nivel: 4 · revisar: 2026-08-28

**Evidências** (mais recente primeiro)
- 2026-08-12 — acertou sem ajuda: distinguiu deslocamento da curva de movimento ao longo dela
- 2026-08-03 — acertou sem ajuda: listou os 4 determinantes de deslocamento

## [[elasticidade-preco]]
estado: em_desenvolvimento · nivel: 1 · revisar: 2026-08-13

**Evidências**
- 2026-08-12 — errou: classificou bem de luxo como inelástico, invertendo a lógica de
  substitutos → [[2026-08-12-economia]]
- 2026-08-12 — acertou com hesitação: escreveu a fórmula, travou ao interpretar o sinal

**Confusões**
- mistura com [[elasticidade-renda]]: usa "renda" querendo dizer "preço"

**Próximo passo**
Classificar 3 bens e justificar pelo critério de substitutos. 3/3 → sobe para nível 2.
```

Regras:
- Ordene os blocos por urgência: revisão vencida no topo, depois `fragil`, depois o resto.
- Mantenha **no máximo 5 evidências** por conceito. Ao passar disso, corte a mais antiga —
  o histórico completo está em `SESSIONS/`.
- Evidência sem descrição do que exatamente falhou é inútil. "errou" não é evidência.
- Arquivo passou de ~300 linhas → divida por tema: `estado-economia-micro.md`,
  `estado-economia-macro.md`, e registre a divisão no `INICIO.md` e no `index.md`.

### Perfil

`LEARNER/perfil.md` — o que vale para todas as disciplinas: objetivos, tempo disponível,
como ele aprende melhor, padrões de erro que se repetem entre assuntos. Muda raramente.

---

## 5. Sessão

`SESSIONS/AAAA-MM-DD-<disciplina>.md`. Se houver duas sessões da mesma disciplina no mesmo
dia, sufixe: `-2`.

**Não é transcript.** É o registro do que mudou. Quem quer o transcript tem o histórico do chat.

```markdown
---
tipo: sessao
disciplina: economia
data: 2026-08-12
duracao_aprox: 40min
---

# 2026-08-12 — Economia

**Objetivo:** fechar a lacuna em elasticidade-preço aberta na sessão anterior.

## Conceitos trabalhados
- [[elasticidade-preco]] — avaliado, errou e depois corrigiu
- [[oferta-e-demanda]] — revisão agendada, passou

## O que aconteceu
- Perguntei como ele classificaria um bem de luxo. Respondeu "inelástico, porque é caro".
  O erro é tratar preço alto como sinal de inelasticidade — o critério é substituto, não preço.
- Depois da correção, classificou 2 de 3 bens certo.

## Mudanças de estado
- [[elasticidade-preco]]: nao_iniciado → em_desenvolvimento (nível 1, revisar 2026-08-13)
- [[oferta-e-demanda]]: nível 3 → 4 (revisar 2026-08-28)

## Lacunas abertas
- Elasticidade cruzada: nunca tocada, e as fontes atuais cobrem pouco.

## Próxima sessão
Começar pela revisão de [[elasticidade-preco]] com 3 classificações. Se passar, entrar em
[[receita-total]], que é onde elasticidade vira decisão prática.
```

---

## 6. INICIO.md (cache de retomada)

Reescrito ao fim de toda sessão. É **derivado** — se conflitar com `LEARNER/`, o LEARNER vence.
Curto por design: se crescer, perde a função. Formato no próprio arquivo, na raiz do vault.

---

## 7. index.md

`SYSTEM/index.md` — catálogo de conteúdo: uma linha por página, com resumo de uma frase.
O valor dele é o resumo (que o sistema de arquivos não tem), não a lista.

Organizado por disciplina → conceitos, fontes, mapa, estado.
**Não lista sessões** — sessões são cronológicas e vivem no `log.md`.

Atualizado em todo INGEST e sempre que uma página é criada, renomeada ou removida.

---

## 8. log.md

`SYSTEM/log.md` — append-only. Prefixo fixo para ser parseável:

```
## [AAAA-MM-DD] <operacao> | <disciplina ou alvo>
```

Operações: `ingest`, `study`, `review`, `update`, `lint`, `system`.

Três a seis linhas por entrada. O log é linha do tempo, não relatório — o detalhe está na
sessão ou na página.

Ao virar o ano, arquive: `SYSTEM/log-2026.md` e comece um `log.md` novo.

---

## 9. Frontmatter — campos válidos

| Campo | Onde | Valores |
|---|---|---|
| `tipo` | todas | `conceito` `fonte` `mapa` `estado` `sessao` `perfil` |
| `disciplina` | todas | kebab-case, igual ao nome da pasta |
| `titulo` | conceito, fonte | texto livre |
| `fontes` | conceito | lista de nomes de arquivo de fonte |
| `arquivo_raw` | fonte | caminho relativo dentro de `RAW/` |
| `criado` / `atualizado` | conceito, mapa, estado | `AAAA-MM-DD` |
| `ingerido` | fonte | `AAAA-MM-DD` |
| `data` | sessao | `AAAA-MM-DD` |

**Não existe** campo de nota, score, porcentagem ou dificuldade. Se aparecer um, é bug.
Estado e nível moram no corpo do LEARNER, não no frontmatter, porque mudam por conceito e
não por arquivo.
