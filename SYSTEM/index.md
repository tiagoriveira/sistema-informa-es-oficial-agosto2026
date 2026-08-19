# INDEX — catálogo do vault

Uma linha por página, com a ideia central resumida. O valor deste arquivo é o **resumo**
(que o sistema de arquivos não tem), não a lista de nomes.

A IA lê este arquivo antes de abrir páginas, para decidir o que abrir. Ele não substitui a
leitura da página.

Sessões **não** entram aqui — são cronológicas e ficam em [[log]].

Atualizado em: 2026-08-18

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
Grade: 5 fases, 27 tópicos (checada na web em 2026-08-14).
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
Grade: 4 fases, 16 tópicos (checada na web em 2026-08-15). A ferramenta de avaliar argumento —
irmã de [[mapa-historia-da-filosofia]], não a mesma coisa. Sem conceito com página ainda.

**3. [[mapa-frameworks-de-pensamento]]** — Frameworks de Pensamento · [[estado-frameworks-de-pensamento]]
Grade: 6 fases, 36 tópicos (checada na web em 2026-08-16). Modelos mentais e decisão sob
incerteza — lógica avalia argumento pronto, aqui escolhe-se a lente pra atacar problema novo.
Maior grade do vault, por pedido explícito de cobertura máxima. Sem conceito com página ainda.

### 💼 negocios

**[[mapa-product-discovery]]** — Product Discovery · [[estado-product-discovery]]
Grade: 4 fases, 18 tópicos.
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

**[[mapa-visao-estrategica-negocios]]** — Visão Estratégica · [[estado-visao-estrategica-negocios]]
Grade: 5 fases, 23 tópicos. Sem conceito com página ainda.

**[[mapa-economia]]** — Economia · [[estado-economia]]
Grade: 4 fases, 17 tópicos (checada na web em 2026-08-15). Micro → macro → comportamental →
aplicação. Sem conceito com página ainda.

**[[mapa-teoria-dos-jogos-e-estrategia]]** — Teoria dos Jogos e Estratégia ·
[[estado-teoria-dos-jogos-e-estrategia]]
Grade: 4 fases, 22 tópicos (checada na web em 2026-08-16). Decisão quando o resultado depende
da jogada de outro jogador racional — irmã de [[mapa-frameworks-de-pensamento]], não a mesma
coisa. Sem conceito com página ainda.

### 🤖 inteligencia-artificial

**Sequência recomendada:** colaboração humano-IA → arquitetura de agentes e contexto (a
camada conceitual/decisão vem antes da camada de arquitetura aplicada que a implementa).

**1. [[mapa-colaboracao-humano-ia]]** — Colaboração Humano-IA · [[estado-colaboracao-humano-ia]]
Grade: 5 fases, 19 tópicos (checada na web em 2026-08-14).
- [[operador-centauro]] — humano planeja/decide, IA executa; vs. oráculo e centauro reverso

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
Grade: 5 fases, 30 tópicos (checada na web em 2026-08-14). Sem conceito com página ainda.

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
Grade: 4 fases, 12 tópicos (checada na web em 2026-08-15). O corpo (sono, energia) — irmã de
[[mapa-gestao-de-tempo]]. Sem conceito com página ainda.

**[[mapa-gestao-de-tempo]]** — Gestão de Tempo · [[estado-gestao-de-tempo]]
Grade: 4 fases, 14 tópicos (checada na web em 2026-08-15). A estrutura (calendário,
prioridade) — irmã de [[mapa-produtividade-biohacking]]. Sem conceito com página ainda.

### 📣 marketing

**[[mapa-marketing]]** — Marketing · [[estado-marketing]]
Grade: 5 fases, 27 tópicos (checada na web em 2026-08-14).
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

**[[mapa-estatistica-para-decisao-marketing]]** — Estatística para Decisão em Marketing ·
[[estado-estatistica-para-decisao-marketing]]
Grade: 4 fases, 16 tópicos (checada na web em 2026-08-19). Criada a partir de autoavaliação do
Tiago — ler/interpretar dado é o ponto fraco declarado em marketing. Separada de
[[mapa-dados-estatistica-e-ia-ml]] (aquela é técnica/ML, esta é decisão de negócio). Sem
conceito com página ainda.

**[[mapa-producao-de-conteudo]]** — Produção de Conteúdo · [[estado-producao-de-conteudo]]
Grade: 5 fases, 23 tópicos (checada na web em 2026-08-15). O ofício de virar conceito em post
por plataforma — irmã de [[mapa-marketing]], não a mesma coisa.
- [[pipeline-de-repurposing]] — um conceito, três formatos, sem repetir pesquisa
- [[mecanica-por-plataforma]] — sinal-chave de cada rede (Instagram/TikTok/Shorts/LinkedIn/Threads-X)

**[[mapa-copywriting]]** — Copywriting · [[estado-copywriting]]
Grade: 4 fases, 16 tópicos (checada na web em 2026-08-15). A frase que persuade — irmã de
[[mapa-producao-de-conteudo]], não a mesma coisa.
- [[fud-competitivo]] — medo real + categoria concorrente desqualificada + autoridade própria

### 🧠 psicologia (hub novo, 2026-08-15)

**[[mapa-psicologia]]** — Psicologia · [[estado-psicologia]]
Grade: 4 fases, 14 tópicos (checada na web em 2026-08-15). Resolve pendência de 2026-08-15
("hub da área da mente"). Sem conceito com página ainda.

### 🤝 dinamicas-sociais (hub novo, 2026-08-15)

**[[mapa-poder-e-dinamica-social]]** — Poder e Dinâmica Social · [[estado-poder-e-dinamica-social]]
Grade: 4 fases, 13 tópicos (checada na web em 2026-08-15). Maquiavel, persuasão, poder em
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
Grade: 4 fases, 16 tópicos (checada na web em 2026-08-17). Capstone do hub — atração como
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
Grade: 5 fases, 25 tópicos, pessoal → corporativo (checada na web em 2026-08-14).
Área sensível a fonte errada — ver aviso no mapa. Sem conceito com página ainda.

### 🗣️ comunicacao

**[[mapa-ingles]]** — Inglês · [[estado-ingles]]
Grade: 5 fases, 30 tópicos, por nível CEFR (A1→C2). Formato adaptado — ver nota no mapa.
Sem conceito com página ainda.

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
estrutura que o Tiago já usa no Notion. Nenhum é fonte. `PROJETOS/`, `AREAS/` e `ARQUIVADOS/`
ainda vazios — ver `LEIA-ME.md` de cada um.

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

**ARQUIVADOS/** — inativo, registro de raciocínio encerrado:
- [[ementa-mapa-status-visual]] — validada e implementada em 2026-08-14, migrada de `ideias/`

**Fora da raiz, em `Videos e cursos que estou acompanhando.md`:** watch-list de cursos/vídeos
(Obsidian ×3, Faggion) — arquivo de acesso rápido, não segue o formato PARA de propósito.

---

## Ideias e produto

`ideias/` é a pasta ativa para ideias pessoais, de produto ou de operação em maturação. Quando
uma ideia ganhar compromisso, ela vai para o destino adequado do PARA.

- [[operacao-prestacao-servicos-multiempresa]] — manter o vault agnóstico e isolar cada cliente
  dentro de uma futura área de prestação de serviços
- [[dashboard-curriculo-progresso]] — currículo e painel visual derivados do LEARNER, ainda em
  maturação
- [[inbox-notas-pessoais]] — registro histórico da decisão que criou a camada de INBOX e PARA
