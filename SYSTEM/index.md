# INDEX — catálogo do vault

Uma linha por página, com a ideia central resumida. O valor deste arquivo é o **resumo**
(que o sistema de arquivos não tem), não a lista de nomes.

A IA lê este arquivo antes de abrir páginas, para decidir o que abrir. Ele não substitui a
leitura da página.

Sessões **não** entram aqui — são cronológicas e ficam em [[log]].

Atualizado em: 2026-08-15 (2)

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
curricular em fases no seu mapa.

### 🧠 neurociencia

**[[mapa-neurociencia-esportiva]]** — Neurociência Esportiva · [[estado-neurociencia-esportiva]]
Grade: 5 fases, 27 tópicos (checada na web em 2026-08-14).
- [[foco-atencional-nideffer]] — largura/direção da atenção, quatro quadrantes
- [[choking-sob-pressao]] — reinvestimento vs. distração sob pressão

### 🏃 esporte

**[[mapa-performance-esportiva]]** — Performance Esportiva · [[estado-performance-esportiva]]
Grade: 5 fases, 21 tópicos (checada na web em 2026-08-15). Fisiologia do esforço (VO2 max,
limiar, força, periodização) — irmã de [[mapa-neurociencia-esportiva]], não a mesma coisa.
- [[tres-sistemas-energeticos]] — fosfagênio/glicolítico/oxidativo, janelas de duração
- [[atp-cp]] — reação única (fosfocreatina→ADP), recuperação em duas fases (~30s / 3-5min)
- [[mito-do-lactato]] — H+ causa a queimação, lactato é combustível, DOMS é micro-lesão

### 📐 filosofia

**[[mapa-historia-da-filosofia]]** — História da Filosofia · [[estado-historia-da-filosofia]]
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

**[[mapa-logica-e-epistemologia]]** — Lógica e Epistemologia · [[estado-logica-e-epistemologia]]
Grade: 4 fases, 16 tópicos (checada na web em 2026-08-15). A ferramenta de avaliar argumento —
irmã de [[mapa-historia-da-filosofia]], não a mesma coisa. Sem conceito com página ainda.

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

**[[mapa-visao-estrategica-negocios]]** — Visão Estratégica · [[estado-visao-estrategica-negocios]]
Grade: 5 fases, 23 tópicos. Sem conceito com página ainda.

**[[mapa-economia]]** — Economia · [[estado-economia]]
Grade: 4 fases, 17 tópicos (checada na web em 2026-08-15). Micro → macro → comportamental →
aplicação. Sem conceito com página ainda.

### 🤖 inteligencia-artificial

**[[mapa-colaboracao-humano-ia]]** — Colaboração Humano-IA · [[estado-colaboracao-humano-ia]]
Grade: 5 fases, 19 tópicos (checada na web em 2026-08-14).
- [[operador-centauro]] — humano planeja/decide, IA executa; vs. oráculo e centauro reverso

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
[[mapa-gestao-conhecimento-second-brain]]. Tem seção de recursos externos (cursos/vídeos).
- [[comandos-e-hotkeys-obsidian]] — a paleta `Ctrl+P` é a porta única; atalho dedicado só pro
  que roda todo dia. Página 100% de conhecimento externo, datada — doc oficial vence.

**[[mapa-produtividade-biohacking]]** — Produtividade & Biohacking · [[estado-produtividade-biohacking]]
Grade: 4 fases, 12 tópicos (checada na web em 2026-08-15). O corpo (sono, energia) — irmã de
[[mapa-gestao-de-tempo]]. Sem conceito com página ainda.

**[[mapa-gestao-de-tempo]]** — Gestão de Tempo · [[estado-gestao-de-tempo]]
Grade: 4 fases, 14 tópicos (checada na web em 2026-08-15). A estrutura (calendário,
prioridade) — irmã de [[mapa-produtividade-biohacking]]. Sem conceito com página ainda.

### 📣 marketing

**[[mapa-marketing]]** — Marketing · [[estado-marketing]]
Grade: 5 fases, 27 tópicos (checada na web em 2026-08-14). Sem conceito com página ainda.

**[[mapa-producao-de-conteudo]]** — Produção de Conteúdo · [[estado-producao-de-conteudo]]
Grade: 5 fases, 23 tópicos (checada na web em 2026-08-15). O ofício de virar conceito em post
por plataforma — irmã de [[mapa-marketing]], não a mesma coisa. Sem conceito com página ainda.

**[[mapa-copywriting]]** — Copywriting · [[estado-copywriting]]
Grade: 4 fases, 16 tópicos (checada na web em 2026-08-15). A frase que persuade — irmã de
[[mapa-producao-de-conteudo]], não a mesma coisa. Sem conceito com página ainda.

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

### 💰 financas

**[[mapa-financas]]** — Finanças · [[estado-financas]]
Grade: 5 fases, 25 tópicos, pessoal → corporativo (checada na web em 2026-08-14).
Área sensível a fonte errada — ver aviso no mapa. Sem conceito com página ainda.

### 🗣️ comunicacao

**[[mapa-ingles]]** — Inglês · [[estado-ingles]]
Grade: 5 fases, 30 tópicos, por nível CEFR (A1→C2). Formato adaptado — ver nota no mapa.
Sem conceito com página ainda.

---

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
  em [[ARQUITETURA]]
- [[referencia-hub-ai-gravacao-servicos-manuais]] — bookmark de startup existente (não é ideia
  própria do Tiago)
- [[tabela-peso-ideal-altura]] — bookmark solto (X/Twitter)
- [[dashboard-curriculo-progresso]] — migrada de `ideias/`, ainda em maturação

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

`ideias/`, `backlog/` e `roadmap/` foram **fundidos ao PARA em 2026-08-15** (ver seção acima).
Só resta em `ideias/`: [[inbox-notas-pessoais]] — deixado fora do PARA por decisão do Tiago,
é mais log de decisão de arquitetura deste vault do que ideia de produto solta.
