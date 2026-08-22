# INDEX — catálogo do vault

Uma linha por página, com a ideia central resumida. O valor deste arquivo é o **resumo**
(que o sistema de arquivos não tem), não a lista de nomes.

A IA lê este arquivo antes de abrir páginas, para decidir o que abrir. Ele não substitui a
leitura da página.

Sessões **não** entram aqui — são cronológicas e ficam em [[log]].

Atualizado em: 2026-08-20

---

## Sistema

- [[INICIO]] — estado atual, disciplina ativa, revisões vencidas, próxima ação
- `CLAUDE.md` — constituição operacional: regras que a IA segue sempre
- [[schema]] — formato de cada tipo de página + estrutura de pastas
- [[log]] — linha do tempo append-only de tudo que foi feito
- [[ARQUITETURA]] — decisões de projeto, mudanças em relação ao briefing, limitações
- [[FAQ]] — uso cotidiano e boas práticas
- [[perfil]] — perfil do aluno, válido para todas as disciplinas

---

## Disciplinas

Estrutura: **hub → disciplina → fase** (ver [[schema]] §0). Toda disciplina tem grade
curricular em fases no seu mapa. Dentro de cada hub, as disciplinas aparecem na sequência
pedagógica recomendada: pré-requisito → integração → aplicação.

### 🧠 neurociencia

**[[mapa-neurociencia-esportiva]]** — Neurociência Esportiva · [[estado-neurociencia-esportiva]]
Grade: 6 fases, 41 tópicos.
- [[sistema-motor]] — córtex, via corticoespinhal, cerebelo e gânglios da base cooperando
- [[propriocepcao-feedback-sensorial]] — os três proprioceptores e o feedback pro cerebelo
- [[malha-aberta-vs-fechada]] — o atraso sensório-motor que decide se dá pra corrigir
- [[unidades-motoras-e-recrutamento]] — princípio do tamanho de Henneman
- [[estagios-aprendizagem-motora]] — cognitivo → associativo → autônomo (Fitts & Posner)
- [[foco-atencional-nideffer]] — largura/direção da atenção, quatro quadrantes
- [[choking-sob-pressao]] — reinvestimento vs. distração sob pressão

### 🏃 esporte

**[[mapa-performance-esportiva]]** — Performance Esportiva · [[estado-performance-esportiva]]
Grade: 5 fases, 21 tópicos (checada na web em 2026-08-15). Fisiologia do esforço (VO2 max,
limiar, força, periodização) — irmã de [[mapa-neurociencia-esportiva]], não a mesma coisa.
- [[tres-sistemas-energeticos]] — fosfagênio/glicolítico/oxidativo, janelas de duração
- [[atp-cp]] — reação única (fosfocreatina→ADP), recuperação em duas fases (~30s / 3-5min)
- [[mito-do-lactato]] — H+ causa a queimação, lactato é combustível, DOMS é micro-lesão

### 📐 [[hub-filosofia]]

**Sequência recomendada:** história da filosofia → lógica e epistemologia → frameworks de
pensamento (contexto → ferramenta de avaliar argumento → aplicação em decisão).

**1. [[mapa-historia-da-filosofia]]** — História da Filosofia · [[estado-historia-da-filosofia]]
Grade: 6 fases, 33 tópicos (dos pré-socráticos à filosofia da mente).

*Fase 1 — Pré-socráticos*
- [[mito-para-logos]] — Tales de Mileto e a virada de explicação mítica para racional
- [[anaximandro-apeiron]] — arché precisa ser indeterminado, não um elemento observável
- [[anaximenes-ar]] — ar como arché, com mecanismo de rarefação/condensação
- [[heraclito-fluxo-e-logos]] — tudo muda, governado por uma ordem racional
- [[parmenides-ser-imutavel]] — mudança é ilusão dos sentidos, o ser é uno e imóvel
- [[empedocles-quatro-raizes]] — quatro elementos eternos, unidos/separados por Amor e Discórdia
- [[democrito-atomismo]] — átomos eternos e vazio, materialismo mecanicista

*Fase 2 — Virada antropológica*
- [[sofistas-relativismo]] — relativismo, "o homem é a medida de todas as coisas"
- [[socrates-metodo-elenchos]] — busca por definição universal, desmonta por contradição

**2. [[mapa-logica-e-epistemologia]]** — Lógica e Epistemologia · [[estado-logica-e-epistemologia]]
Grade: 7 fases, 39 tópicos. A ferramenta de avaliar argumento —
irmã de [[mapa-historia-da-filosofia]], não a mesma coisa. Sem conceito com página ainda.

**3. [[mapa-frameworks-de-pensamento]]** — Frameworks de Pensamento · [[estado-frameworks-de-pensamento]]
Grade: 6 fases, 36 tópicos (checada na web em 2026-08-16). Modelos mentais e decisão sob
incerteza — lógica avalia argumento pronto, aqui escolhe-se a lente pra atacar problema novo.
Maior grade do vault, por pedido explícito de cobertura máxima. Sem conceito com página ainda.

### 💼 negocios

**Sequência recomendada** (definida em 2026-08-20, ao criar product-management): mecanismo
econômico → onde competir → decisão estratégica com outro jogador → o que construir → como se
faz o ofício de produto.

**1. [[mapa-economia]]** — Economia · [[estado-economia]]
Grade: 6 fases, 38 tópicos. Como a economia pensa → preço → consumidor e firma → estruturas e
falhas → macro → as escolas em disputa, comportamental e aplicação. Sem conceito com página.

**2. [[mapa-visao-estrategica-negocios]]** — Visão Estratégica · [[estado-visao-estrategica-negocios]]
Grade: 6 fases, 47 tópicos. O que é estratégia → existe negócio aqui → onde competir → fossos
e as sete potências → modelo de negócio e capital → decidir e executar. Sem conceito com página.

**3. [[mapa-teoria-dos-jogos-e-estrategia]]** — Teoria dos Jogos e Estratégia ·
[[estado-teoria-dos-jogos-e-estrategia]]
Grade: 4 fases, 22 tópicos (checada na web em 2026-08-16). Decisão quando o resultado depende
da jogada de outro jogador racional — irmã de [[mapa-frameworks-de-pensamento]], não a mesma
coisa. Sem conceito com página ainda.

**4. [[mapa-product-discovery]]** — Product Discovery · [[estado-product-discovery]]
Grade: 4 fases, 22 tópicos.
- [[validacao-de-problema]] — confirmar a dor antes de construir
- [[riscos-de-descoberta]] — os quatro riscos além do valor (Cagan)
- [[mvp-e-tipos-de-experimento]] — experimento certo pra cada risco
- [[jobs-to-be-done]] — o "job" que o cliente contrata (concorrência real)
- [[outcome-vs-output]] — medir mudança real, não entrega
- [[continuous-discovery]] — descoberta como prática contínua (Torres)
- [[dual-track-agile]] — descoberta e entrega rodando em paralelo
- [[over-serving-e-job-mal-atendido]] — produto que atende demais uma dimensão, mal atende a
  que decide a contratação (fora da grade)
- [[consistencia-job-narrativa-produto]] — job definido pelo resultado vira régua pra
  narrativa, posicionamento e produto; princípio original do Tiago (fora da grade)

**5. [[mapa-product-management]]** — Product Management · [[estado-product-management]]
_(disciplina nova, 2026-08-20)_ Grade: 4 fases, 21 tópicos. O **ofício** de produto — cargo,
time empoderado × time de funcionalidade, priorização, roadmap, estratégia, métricas e
influência sem autoridade. Descoberta continua sendo de [[mapa-product-discovery]]. Sem
conceito com página ainda.

### 🤖 inteligencia-artificial

**Sequência recomendada:** colaboração humano-IA → arquitetura de agentes e contexto (a
camada conceitual/decisão vem antes da camada de arquitetura aplicada que a implementa).

**1. [[mapa-colaboracao-humano-ia]]** — Colaboração Humano-IA · [[estado-colaboracao-humano-ia]]
Grade: 5 fases, 19 tópicos (checada na web em 2026-08-14).
- [[operador-centauro]] — humano planeja/decide, IA executa; vs. oráculo e centauro reverso
- [[complementaridade-homem-maquina]] — humano e máquina não competem pelo mesmo trabalho, e é
  a combinação que gera vantagem difícil de copiar (Thiel, *Zero to One* cap. 12); fora da grade

**2. [[mapa-arquitetura-de-agentes-e-contexto]]** — Arquitetura de Agentes e Contexto ·
[[estado-arquitetura-de-agentes-e-contexto]]
Grade: 5 fases, 20 tópicos (checada na web em 2026-08-19). Como estruturar arquivo de
contexto (CLAUDE.md/AGENTS.md), skills, pipeline de ingestão e orquestração multi-agente —
camada aplicada e agnóstica de domínio (serve pra negócio, second brain ou qualquer sistema).
Criada a pedido do Tiago em 2026-08-19, a partir do curso "Ratos OS" + resposta do Grok — ver
"Fronteiras" no mapa pra não confundir com [[mapa-colaboracao-humano-ia]],
[[mapa-dados-estatistica-e-ia-ml]] e [[mapa-gestao-conhecimento-second-brain]]. Sem conceito
com página ainda.

### ⚙️ gestao-sistemas

**[[mapa-fundamentos-sistemas-gestao]]** — Fundamentos de Sistemas & Gestão · [[estado-fundamentos-sistemas-gestao]]
Grade: 7 fases, 40 tópicos. Sem conceito com página ainda.

**[[mapa-gestao-conhecimento-second-brain]]** — Gestão do Conhecimento & Second Brain · [[estado-gestao-conhecimento-second-brain]]
Grade: 5 fases, 21 tópicos (checada na web em 2026-08-14).
- [[arquivo-morto]] — capturar não é saber; acúmulo bloqueia até a busca
- [[ciclo-code]] — cada etapa obriga a informação a mudar de forma
- [[captura-seletiva]] — ressonância como filtro de entrada
- [[nota-efemera-vs-permanente]] — a janela de 24-48h e por que ela existe

**[[mapa-obsidian]]** — Obsidian · [[estado-obsidian]]
Grade: 5 fases, 27 tópicos (checada na web em 2026-08-15). A **ferramenta**; o método fica em
[[mapa-gestao-conhecimento-second-brain]]. Primeiras fontes próprias em `RAW/obsidian/` desde
2026-08-18 (2 papers + 1 artigo prático), sem página de fonte dedicada.
- [[comandos-e-hotkeys-obsidian]] — a paleta `Ctrl+P` é a porta única; atalho dedicado só pro
  que roda todo dia. Página 100% de conhecimento externo, datada — doc oficial vence.
- [[principios-duraveis-pkm-ia]] — 6 princípios de PKM+IA que não dependem de modelo,
  benchmark ou ferramenta específicos

**[[mapa-produtividade-biohacking]]** — Produtividade & Biohacking · [[estado-produtividade-biohacking]]
Grade: 7 fases, 34 tópicos. O corpo (sono, energia) — irmã de
[[mapa-gestao-de-tempo]]. Sem conceito com página ainda.

**[[mapa-gestao-de-tempo]]** — Gestão de Tempo · [[estado-gestao-de-tempo]]
Grade: 4 fases, 14 tópicos (checada na web em 2026-08-15). A estrutura (calendário,
prioridade) — irmã de [[mapa-produtividade-biohacking]]. **14 páginas escritas em 2026-08-22**,
todas `📖`, zero avaliadas.
- [[matriz-eisenhower]] — urgente ≠ importante; a matriz 2×2 é de Covey (1989), não Eisenhower
- [[pareto-aplicado-a-tarefas]] — poucas tarefas concentram a maior parte do resultado
- [[coma-o-sapo]] — fazer primeiro a tarefa mais evitada, enquanto a energia está intacta
- [[custo-invisivel-de-dizer-sim-a-tudo]] — todo aceite é um "não" implícito a outra coisa
- [[time-blocking]] — reservar horário fixo pra tarefa específica, não só listar
- [[deep-work]] — blocos protegidos de foco pra trabalho cognitivamente exigente
- [[custo-de-trocar-de-tarefa]] — switch cost + resíduo de atenção, por que multitarefa rende menos
- [[buffer-na-agenda]] — folga deliberada pra agenda não quebrar no primeiro imprevisto
- [[gestao-de-energia-vs-gestao-de-tempo]] — hora não vale o mesmo o dia inteiro
- [[tarefa-exigente-no-pico-de-energia]] — tarefa exigente no pico, administrativa no vale
- [[pausa-como-parte-do-sistema]] — pausa recupera a capacidade que o trabalho consome
- [[sistema-demais-quebra-primeiro]] — empilhar técnica demais é o que derruba o sistema
- [[revisao-semanal]] — o hábito que corrige o sistema antes dele degradar em silêncio
- [[quando-abandonar-uma-tecnica]] — técnica que parou de mudar decisão virou ritual vazio

### 📣 marketing

**Sequência recomendada** (definida em 2026-08-20, ao criar marketing-tecnico e
growth-e-retencao): o mapa geral → a mensagem → o ativo publicado → a execução e a medição →
ler o número que a execução produz → o sistema que faz crescer e reter.

**1. [[mapa-marketing]]** — Marketing · [[estado-marketing]]
Grade: 7 fases, 48 tópicos. Fundamentos, preço, canais, conteúdo, medição, IA na operação, e
dado/personalização/risco.
- [[criacao-e-captura-de-demanda]] — marketing cria e captura demanda a partir do job real do
  cliente; propaganda é só uma ferramenta dentro disso, conecta com [[jobs-to-be-done]]
- [[ia-pesquisa-posicionamento-concorrencia]] — IA transforma pesquisa de concorrência em
  monitoramento contínuo, do preço ao criativo ao briefing de vendas
- [[ia-producao-de-conteudo-e-criativo]] — escala volume/adaptação, mas tende ao genérico;
  ângulo criativo e aprovação final continuam humanos
- [[automacao-de-campanha-e-verba]] — humano define métrica-alvo e teto, IA aloca verba em
  tempo real
- [[julgamento-humano-obrigatorio-marketing]] — aplica [[operador-centauro]] às três anteriores;
  distingue oráculo (falta de critério) de centauro reverso (desconfiança do critério)
- [[problema-de-distribuicao-vs-demanda]] — recompra alta com crescimento travado é gargalo de
  canal, não de demanda (fora da grade)
- [[marketing-de-influencia-e-co-marketing]] · [[marketing-de-afiliados]] — os dois canais de
  audiência emprestada, com a regra brasileira de identificação publicitária revisada em 2026
- [[agente-autonomo-de-marketing]] · [[answer-engine-optimization]] · [[first-party-data]] ·
  [[hiperpersonalizacao-em-escala]] · [[otimizacao-dinamica-de-criativo]] · [[churn-preditivo]] ·
  [[chatbot-de-conversao]] · [[direito-autoral-em-conteudo-de-ia]] — as Fases 6 e 7

**2. [[mapa-copywriting]]** — Copywriting · [[estado-copywriting]]
Grade: 5 fases, 33 tópicos, **todos com página escrita** (2026-08-20). A frase que persuade —
irmã de [[mapa-producao-de-conteudo]], não a mesma coisa.
- *Fundamentos:* [[copy-como-venda-por-escrito]] · [[hierarquia-de-impacto-em-copy]] ·
  [[copy-canaliza-desejo-existente]] · [[clareza-e-especificidade]] ·
  [[beneficio-vs-caracteristica]] · [[hierarquia-de-prova]]
- *Pesquisa, consciência e oferta:* [[pesquisa-de-linguagem-do-cliente]] ·
  [[entrevista-de-copy-o-gatilho]] · [[mapeamento-de-objecoes]] · [[niveis-de-consciencia]] ·
  [[sofisticacao-de-mercado]] · [[anatomia-da-oferta]]
- *Anatomia e frameworks:* [[anatomia-da-peca-de-copy]] · [[headline]] · [[tipos-de-hook]] ·
  [[frameworks-de-copy]] · [[mecanismo-unico]] · [[persuasao-e-seus-limites]] ·
  [[chamada-para-acao]] · [[fud-competitivo]] (fora da grade)
- *Canal, edição e medição:* [[copy-por-canal]] · [[copy-b2b-e-servico-local]] ·
  [[angulo-de-copy]] · [[ritmo-e-protocolo-de-edicao]] · [[cortar-o-rascunho]] ·
  [[medir-copy-por-etapa]] · [[teste-ab-de-copy]]
- *IA aplicada à copy:* [[forcas-e-riscos-da-ia-em-copy]] · [[workflow-de-copy-com-ia]] ·
  [[prompt-de-copy]] · [[contexto-persistente-de-copy]] · [[texto-com-cara-de-ia]] ·
  [[escala-de-copy-sem-spam]] · [[claim-inventado-e-verificacao]]

**3. [[mapa-producao-de-conteudo]]** — Produção de Conteúdo · [[estado-producao-de-conteudo]]
Grade: 7 fases, 31 tópicos. O ofício de virar conceito em post por plataforma — irmã de
[[mapa-marketing]], não a mesma coisa.
- [[pipeline-de-repurposing]] — um conceito, três formatos, sem repetir pesquisa
- [[mecanica-por-plataforma]] — sinal-chave de cada rede
- [[funil-de-conteudo]] · [[storytelling-de-marca]] · [[newsletter-como-midia-propria]] ·
  [[entrevista-e-podcast-de-marca]] — formatos de ativo próprio (Fase 6)
- [[seo-de-conteudo-e-autoridade-topica]] · [[conteudo-gerado-pelo-usuario]] ·
  [[operacao-de-comunidade]] · [[personal-branding-como-canal]] — audiência e comunidade (Fase 7)

**4. [[mapa-marketing-tecnico]]** — Marketing Técnico · [[estado-marketing-tecnico]]
_(disciplina nova, 2026-08-20)_ 18 itens em 4 blocos temáticos, **sem ordem sugerida** —
disciplina de consulta. A camada de execução: rastreamento e medição, plataformas de anúncio,
site e conversão, base de dados e automação. Todos os 18 com página escrita (`📖`), nenhum
avaliado. É a área do vault que envelhece mais rápido.
- [[rastreamento-de-eventos-e-pixel]] · [[medicao-do-lado-do-servidor]] · [[analytics-de-evento]] ·
  [[fim-do-cookie-de-terceiro]] · [[auditoria-tecnica-de-conversao]]
- [[arquitetura-de-campanha-em-ads]] · [[estrategia-de-lance]] ·
  [[remarketing-e-audiencia-personalizada]] · [[midia-programatica-e-curadoria]] · [[dark-social]]
- [[cro-na-pratica]] · [[seo-tecnico]] · [[metricas-de-qualificacao-de-lead]]
- [[crm-como-base-de-marketing]] · [[nutricao-de-leads]] ·
  [[marketing-automation-fluxo-e-gatilho]] · [[automacao-de-fluxo-entre-ferramentas]] ·
  [[scraping-para-inteligencia-competitiva]]

**5. [[mapa-estatistica-para-decisao-marketing]]** — Estatística para Decisão em Marketing ·
[[estado-estatistica-para-decisao-marketing]]
Grade: 4 fases, 16 tópicos (checada na web em 2026-08-20). Criada a partir de autoavaliação do
Tiago — ler/interpretar dado é o ponto fraco declarado em marketing. Separada de
[[mapa-dados-estatistica-e-ia-ml]] (aquela é técnica/ML, esta é decisão de negócio). Sem
conceito com página ainda.

**6. [[mapa-growth-e-retencao]]** — Growth e Retenção · [[estado-growth-e-retencao]]
_(disciplina nova, 2026-08-20)_ 15 itens em 4 blocos temáticos, **sem ordem sugerida**.
Crescimento como sistema: loop em vez de funil, ativação e retenção em vez de só aquisição.
Todos com página escrita (`📖`), nenhum avaliado.
- [[growth-hacking-e-loop-viral]] · [[coeficiente-viral-k-factor]] · [[product-led-growth]] ·
  [[go-to-market-em-novo-mercado]]
- [[onboarding-e-ativacao]] · [[iceberg-da-retencao]] · [[loop-de-retencao-e-habito]] ·
  [[analise-de-coorte]]
- [[north-star-metric]] · [[priorizacao-de-experimento-ice]] · [[okr-de-marketing]] · [[revops]]
- [[community-led-growth]] · [[pricing-como-canal-de-growth]] · [[account-based-marketing]]

### 🧠 psicologia (hub novo, 2026-08-15)

**[[mapa-psicologia]]** — Psicologia · [[estado-psicologia]]
Grade: 4 fases, 14 tópicos (checada na web em 2026-08-15). Resolve pendência de 2026-08-15
("hub da área da mente"). Sem conceito com página ainda.

### 🤝 dinamicas-sociais (hub novo, 2026-08-15)

**[[mapa-poder-e-dinamica-social]]** — Poder e Dinâmica Social · [[estado-poder-e-dinamica-social]]
Grade: 6 fases, 33 tópicos. Maquiavel, capital social, desejo mimético, poder em
geral — irmã de [[mapa-comportamento-masculino-e-realismo]]. Sem conceito com página ainda.

**[[mapa-comportamento-masculino-e-realismo]]** — Comportamento Masculino e Realismo ·
[[estado-comportamento-masculino-e-realismo]]
Grade: 4 fases, 12 tópicos (checada na web em 2026-08-15). Pedido explícito de 2026-08-15
(inspirada no Ybernator/Nessahan, grade desenhada do zero). Sem conceito com página ainda.

**[[mapa-seducao-e-comunidade-pua]]** — Sedução e a Comunidade PUA · [[estado-seducao-e-comunidade-pua]]
Grade: 4 fases, 16 tópicos (checada na web em 2026-08-17). Pedido explícito de 2026-08-17 —
análise crítica da literatura PUA (Mystery, Neil Strauss), não curso de técnica. Inclui caso
documentado de assédio (Julien Blanc). Sem conceito com página ainda.

**[[mapa-identidade-atraente]]** — Identidade Atraente · [[estado-identidade-atraente]]
Grade: 6 fases, 36 tópicos. Capstone do hub — atração como
subproduto de identidade real (autenticidade, valores, hábito identitário), não de tática.
Fecha a sobreposição com [[mapa-comportamento-masculino-e-realismo]] e
[[mapa-seducao-e-comunidade-pua]] de forma explícita. Sem conceito com página ainda.

### ✝️ [[hub-teologia]] (hub novo, 2026-08-16)

**Sequência recomendada:** hermenêutica bíblica → teologia bíblica → história da Igreja →
teologia sistemática → apologética cristã.

**1. [[mapa-hermeneutica-biblica]]** — Hermenêutica Bíblica · [[estado-hermeneutica-biblica]]
Grade: 4 fases, 16 tópicos. Leitura contextual, literária e responsável das Escrituras.
- [[o-que-e-hermeneutica]] — observar, interpretar e aplicar sem confundir as três tarefas

**2. [[mapa-teologia-biblica]]** — Teologia Bíblica · [[estado-teologia-biblica]]
Grade: 4 fases, 16 tópicos. Temas e narrativa através do cânon bíblico. Sem conceito com página ainda.

**3. [[mapa-historia-da-igreja]]** — História da Igreja · [[estado-historia-da-igreja]]
Grade: 4 fases, 16 tópicos. Cristianismos do primeiro século ao mundo contemporâneo. Sem conceito com página ainda.

**4. [[mapa-teologia-sistematica]]** — Teologia Sistemática · [[estado-teologia-sistematica]]
Grade: 4 fases, 17 tópicos. Método, doutrinas cristãs e diferenças entre tradições. Sem conceito com página ainda.

**5. [[mapa-apologetica-crista]]** — Apologética Cristã · [[estado-apologetica-crista]]
Grade: 4 fases, 16 tópicos. Razões, evidências, objeções e diálogo sobre a fé cristã. Sem conceito com página ainda.

### 💰 financas

**[[mapa-financas]]** — Finanças · [[estado-financas]]
Grade: 6 fases, 45 tópicos, pessoal → margem e preço → caixa e estoque → ler o negócio inteiro.
Área sensível a fonte errada — ver aviso no mapa. Sem conceito com página ainda.

### 🗣️ comunicacao

**Sequência recomendada** (definida em 2026-08-20, ao criar as duas disciplinas novas):
estruturar o pensamento por escrito → levar o argumento a alguém que resiste → outra língua,
que é percurso independente. [[mapa-logica-e-epistemologia]] (hub filosofia) é pré-requisito
natural das duas primeiras — é a gramática de ambas.

**1. [[mapa-escrita-e-pensamento-estruturado]]** — Escrita e Pensamento Estruturado ·
[[estado-escrita-e-pensamento-estruturado]]
_(disciplina nova, 2026-08-20)_ Grade: 6 fases, 29 tópicos. Pirâmide, decomposição, SCQA, a
frase, o parágrafo, os formatos, o processo. Texto que **decide** — não texto que vende
([[mapa-copywriting]]) nem formato de plataforma ([[mapa-producao-de-conteudo]]). Sem conceito
com página ainda.

**2. [[mapa-influencia-persuasao-oratoria]]** — Influência, Persuasão e Oratória ·
[[estado-influencia-persuasao-oratoria]]
_(disciplina nova, 2026-08-20)_ Grade: 5 fases, 24 tópicos. Retórica, negociação (interesses ×
posições, BATNA, ZOPA) e oratória. Falácias continuam sendo de
[[mapa-logica-e-epistemologia]]; capital social e poder informal, de
[[mapa-poder-e-dinamica-social]]. Sem conceito com página ainda.

**3. [[mapa-ingles]]** — Inglês · [[estado-ingles]]
Grade: 6 fases, 42 tópicos, por nível CEFR (A1→C2) com uma fase de método na frente. Formato
adaptado — ver nota no mapa. Sem conceito com página ainda.

### 💻 [[hub-tecnologia]] (hub novo, 2026-08-17)

**Sequência recomendada:** fundamentos de programação → engenharia de software → dados/IA-ML →
tecnologia para fundadores. Sem fonte em `RAW/` em nenhuma — todas checadas via busca na web
em 2026-08-17, área que envelhece rápido (ver aviso em cada mapa).

**1. [[mapa-fundamentos-de-programacao]]** — Fundamentos de Programação · [[estado-fundamentos-de-programacao]]
Grade: 5 fases, 24 tópicos. Lógica, estrutura de dado e algoritmo — pré-requisito do hub.
Sem conceito com página ainda.

**2. [[mapa-engenharia-de-software]]** — Engenharia de Software · [[estado-engenharia-de-software]]
Grade: 5 fases, 20 tópicos. Arquitetura, dado, API e design de sistema em escala.
Sem conceito com página ainda.

**3. [[mapa-dados-estatistica-e-ia-ml]]** — Dados, Estatística e IA/ML · [[estado-dados-estatistica-e-ia-ml]]
Grade: 5 fases, 22 tópicos. Estatística → ML clássico → deep learning/LLM → IA agêntica.
Fronteira com [[mapa-colaboracao-humano-ia]] (hub inteligencia-artificial) — ver nota no mapa.
Sem conceito com página ainda.

**4. [[mapa-tecnologia-para-fundadores]]** — Tecnologia para Fundadores · [[estado-tecnologia-para-fundadores]]
Grade: 4 fases, 16 tópicos. Decisão técnica e gestão de time técnico sem programar — capstone
do hub. [[beneficios-obsidian-founder-solo]] — conceito de apoio, fora da numeração da grade.

---

### 🧭 consultoria (hub novo, 2026-08-18)

Hub separado de `negocios`/`marketing`: conhecimento de como prestar consultoria de marketing
pra um cliente específico (diagnóstico, pricing do serviço, métrica de SaaS, distribuição
early-stage) — a camada de cima que aplica [[mapa-marketing]] e [[mapa-product-discovery]]
quando você é o prestador de serviço, não o founder. Sem fonte em `RAW/` — modo exploração.

**1. [[mapa-marketing-para-saas-b2b]]** — Marketing para SaaS B2B (consultoria) ·
[[estado-marketing-para-saas-b2b]]
Grade: 4 fases, 16 tópicos. Origem: parceria real (MVP SaaS financeiro) disparou a
necessidade, mas escopo geral, reutilizável pra qualquer parceria de consultoria futura. Sem
conceito com página ainda.

---


---

## Ybernator — arquivado (2026-08-18)

123 disciplinas foram importadas do Ybernator em 2026-08-18 e arquivadas no mesmo dia, a
pedido do Tiago (desconfiança da curadoria original — ver `ARQUIVADOS/ybernator/LEIA-ME.md`
para o achado real e o critério). Não aparecem nas listas de disciplina abaixo. Estão em
`ARQUIVADOS/ybernator/`, com procedimento definido para promover disciplina individual de
volta pro sistema ativo quando pedido.

## INBOX — notas pessoais (efêmera)

Camada crua, criada em 2026-08-15. **Não é fonte** — não citar como autoridade em KNOWLEDGE.
Ver `INBOX/LEIA-ME.md`. Recebeu 23 capturas diretas em 2026-08-15 (fora do fluxo de chat);
a maioria triada no mesmo dia — ver `SYSTEM/log.md` pra o detalhe de cada uma.

## PARA — destino do INBOX (`PROJETOS/` `AREAS/` `RECURSOS/` `ARQUIVADOS/`)

Substitui a antiga camada `NOTAS/` — decisão de 2026-08-15, método PARA (Tiago Forte), mesma
estrutura que o Tiago já usa no Notion. Nenhum é fonte. `AREAS/` continua vazia (só o Tiago
nomeia uma área) — ver `LEIA-ME.md` de cada um.

**PROJETOS/** — compromisso ativo, com próxima ação clara:
- [[parceria-marketing-mvp-saas-financeiro]] — serviço de marketing para um MVP SaaS
  financeiro, em parceria; pré-início, aguardando alinhamento com o founder
- [[parceria-agencia-marketing-bruno-gasquez]] — liderança estratégica numa agência de
  marketing, tirando o sócio do operacional; pré-início, meta de R$ 25k/mês sem custos ainda
  calculados

**RECURSOS/** (destino padrão, sem prazo/área definida) — referência externa na raiz, reflexão
pessoal em `notas-pessoais/` (separado em 2026-08-15, nunca misturar os dois):
- [[futebol-perfil-fisico-por-posicao]] — exigências físicas do futebol moderno por posição
  (conversa com Grok)
- [[metodo-llm-wiki-karpathy]] — o padrão que inspira o próprio desenho deste vault; linkado
  em [[ARQUITETURA]]. Embed do documento original do Karpathy (`llm-wiki - Copia.md`, também
  em `RECURSOS/` — recuperado da lixeira do OneDrive em 2026-08-15 depois de eu ter apagado
  sem permissão)
- [[founder-solo-ia-operador-centauro]] — fusão de duas notas do Notion (jun/2026),
  atualizada em 2026-08-19 com checagem web (memória de agente como camada separada,
  orquestrador central) — ver seção "O que foi atualizado" no próprio arquivo
- [[referencia-hub-ai-gravacao-servicos-manuais]] — bookmark de startup existente (não é ideia
  própria do Tiago)
- [[tabela-peso-ideal-altura]] — bookmark solto (X/Twitter)
- [[sequoia-services-the-new-software-matheus-beirao]] — Reel transcrito via Apify: tese de que
  IA passa a entregar o trabalho pronto (não só ferramenta), citando relatório da Sequoia
  Capital não verificado nesta sessão
- [[plano-perfeito-army-diagnostico-distribuicao]] — diagnóstico ao vivo de marca de roupa
  fitness: gargalo de distribuição, não de demanda; origem de
  [[problema-de-distribuicao-vs-demanda]]
- [[linkedin-joao-branco-erros-com-agencia]] — cinco pedidos que um ex-CMO não repetiria; o
  padrão é terceirizar à agência o que é responsabilidade intransferível do cliente
- `Comandos e Atalhos Windows.md` — atalhos de Windows, Explorer, PowerShell, git, Claude Code
  e Obsidian (formato de tabela, não segue o padrão PARA)
- `product requirements document - pra q serve.md` — o que é um PRD e o que ele precisa conter
  (com a imagem `Pasted image 20260819105424.png`, que o arquivo referencia)
- `Videos e cursos que estou acompanhando.md` — watch-list viva de cursos e vídeos; movida do
  INBOX em 2026-08-20, continua sendo atualizada pelo Tiago

**RECURSOS/leituras/** (criada em 2026-08-20) — anotação e resumo de livro escritos pelo Tiago:
- `Cap 12 - livro zero to one.md` — nota dele sobre homem-máquina; origem de
  [[complementaridade-homem-maquina]]
- `Livro -- Segundo cérebro Tiago forte … Cap 10 - Página 203.md`

**RECURSOS/transcricoes/** (criada em 2026-08-20) — transcrição e resumo gerados por IA:
- `LOJA DE ROUPAS MIRA R$45 MILHÕES…` (Plano Perfeito #12) · `Transcrição video - Construindo
  Uma Empresa do Zero… Alfredo Soares` · `Video Youtube Bruno Faggion - o que continua valioso…`

**RECURSOS/notas-pessoais/**:
- [[motivacao-por-validacao-externa]] — motivar-se por likes desloca o objetivo da atividade
  para a validação, e o resultado na atividade cai
- [[marco-aurelio-validacao-externa]] — *Meditações* 6.51: fama / prazer / entendimento, e
  onde cada um coloca o próprio bem
- [[comecar-simples-recompensa-no-processo]] — dar o primeiro passo importa mais que começar
  perfeito; recompensa vai no processo, não no resultado final
- [[recompensar-processo-nao-destino-ikigai]] — mesma ideia, capturada de novo com o link pra
  ikigai
- [[reflexao-medicacao-e-conexao-racional]] — reflexão pessoal sobre reinterpretar aproximação
  emocional de forma racional em vez de por estímulo (13/08/2026)
- [[projeto-nao-estruturado-em-para]] — nota ambígua sobre PARA, arquivada sem resolução por
  decisão do Tiago
- [[observacoes-founders-vale-do-silicio]] — três observações próprias: ficção científica como
  viés produtivo, accountability por meta pública, e skin in the game

**ARQUIVADOS/** — inativo, registro de raciocínio encerrado:
- [[ementa-mapa-status-visual]] — validada e implementada em 2026-08-14, migrada de `ideias/`
- `inbox-triado-2026-08/` — capturas cujo conteúdo já foi inteiramente absorvido por páginas do
  vault, guardadas como lastro; tabela de origem→destino no `LEIA-ME.md` da pasta
- `ybernator/` — 123 disciplinas importadas e arquivadas em 2026-08-18

---

## Ideias e produto

`ideias/` é a pasta ativa para ideias pessoais, de produto ou de operação em maturação. Quando
uma ideia ganhar compromisso, ela vai para o destino adequado do PARA.

- [[operacao-prestacao-servicos-multiempresa]] — manter o vault agnóstico e isolar cada cliente
  dentro de uma futura área de prestação de serviços
- [[dashboard-curriculo-progresso]] — currículo e painel visual derivados do LEARNER, ainda em
  maturação
- [[inbox-notas-pessoais]] — registro histórico da decisão que criou a camada de INBOX e PARA
- [[crm-integrado-ia-para-comercial]] — IA lendo o CRM pra extrair objeção recorrente e virar
  pauta de conteúdo; serve aos dois projetos de parceria, ainda sem validação
