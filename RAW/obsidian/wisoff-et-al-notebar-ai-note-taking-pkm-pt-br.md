---
fonte_original: wisoff-et-al-notebar-ai-note-taking-pkm.pdf
traduzido_por: ia
traduzido_em: 2026-08-18
nota: >
  Tradução do corpo científico do paper (arXiv 2509.03610). Tabelas numéricas mantidas
  como no original (números não se traduzem); lista de referências bibliográficas mantida
  em inglês (título de paper não se traduz). Nenhum conteúdo substantivo foi omitido.
---

# NoteBar: Um Sistema de Anotação Assistido por IA para Gestão de Conhecimento Pessoal

**Autores:** Josh Wisoff (NoteBar Research), Yao Tang (University of Rochester), Zhengyu Fang
(Case Western Reserve University), Jordan Guzman (Skidmore College), YuTang Wang (University
of Rochester), Alex Yu (University of Rochester)

## Resumo

Fazer anotações é uma prática crítica para capturar, organizar e refletir sobre informação
tanto em ambientes acadêmicos quanto profissionais. O sucesso recente dos modelos de linguagem
de larga escala (LLMs) acelerou o desenvolvimento de ferramentas assistidas por IA, mas as
soluções existentes costumam ter dificuldade com eficiência. Apresentamos o NoteBar, uma
ferramenta de anotação assistida por IA que usa informação de "persona" e modelos de linguagem
eficientes para organizar notas automaticamente em múltiplas categorias e apoiar melhor os
fluxos de trabalho do usuário. Para apoiar pesquisa e avaliação nessa área, também introduzimos
um dataset inédito condicionado a persona, com 3.173 notas e 8.494 conceitos anotados em 16
personas MBTI, oferecendo diversidade e riqueza semântica para tarefas subsequentes. Por fim,
demonstramos que o NoteBar pode ser implantado de forma prática e econômica, permitindo uso
interativo sem depender de infraestrutura pesada.

## I. Introdução

Fazer anotações é uma prática acadêmica e profissional crítica, já que anotar de forma
eficiente sustenta atenção, compreensão e memória. Funciona tanto como registro externo de
informação quanto como processo cognitivo ativo que facilita codificação e recuperação
posterior. Com a dependência crescente de plataformas digitais, a anotação migrou do papel e
caneta tradicionais para uma ampla gama de sistemas digitais, que oferecem vantagens como
buscabilidade, portabilidade e integração com outras aplicações. Ainda assim, essa transição
também introduz limitações críticas: a anotação digital é inerentemente complexa, já que os
processos de compreensão, resumo e síntese são difíceis de sustentar em ambientes digitais, e
os sistemas existentes frequentemente falham em capturar essas funções de forma eficaz. Além
disso, muitas ferramentas continuam ineficientes, restringindo o usuário a uma entrada rígida
e linear em vez das estruturas flexíveis e organizadas espacialmente que a escrita à mão
permite.

Sistemas digitais de anotação iniciais como StuPad, NoteTaker e Classroom Presenter,
SmartNotes, Tsaap-Notes facilitam a anotação, mas costumam oferecer funções fragmentadas, e
dão suporte apenas parcial à compreensão e síntese. Mais recentemente, surgiram métodos
assistidos por IA: MeetingVis foca em resumo visual em tempo real, NoTeeline expande
micro-anotações do usuário em notas completas usando LLMs, enquanto GazeNoter combina
realidade aumentada e seleção por rastreamento de olhar para copilotar a geração de notas.

Para resolver as limitações dos sistemas de anotação existentes, propomos o NoteBar
(https://notebar.ai/), uma plataforma assistida por IA que unifica classificação, recuperação
e interação do usuário num único fluxo de trabalho. Notas brutas são transformadas em
representações estruturadas para classificação subsequente, enquanto a recuperação sustenta
sugestões contextuais. Um mecanismo de feedback é incorporado para permitir refinamento
iterativo e alinhamento mais forte com a intenção do usuário.

**Contribuições do trabalho:**
- Introduzimos o NoteBar, um sistema inédito de anotação assistida por IA que unifica
  classificação, recuperação e interação do usuário num único pipeline.
- Desenhamos e liberamos um dataset condicionado a persona com 3.173 notas sintéticas e 8.494
  anotações de conceito, permitindo avaliação reproduzível de classificação multi-rótulo de
  notas.
- Fornecemos uma arquitetura pronta para implantação e um estudo preliminar com usuários,
  mostrando que o NoteBar melhora eficiência e engajamento em fluxos de gestão de conhecimento
  pessoal.

## II. Trabalhos Relacionados

**Sistemas e ferramentas de anotação.** A anotação tradicional foi dominada por muito tempo
por métodos de papel e caneta, valorizados pela flexibilidade, imediatismo e forte suporte a
processos cognitivos como compreensão e memória. Com a dependência crescente de plataformas
digitais, ferramentas como Microsoft OneNote e DyKnow surgiram para melhorar portabilidade,
buscabilidade e colaboração — mas frequentemente restringem o usuário a interfaces lineares ou
rígidas e não sustentam as funções integrativas e reflexivas mais profundas da anotação.
Sistemas mais interativos como NoteLook, Classroom Presenter, InkSeine e VideoSticker reduzem
o peso mecânico da escrita manual, mas ainda exigem que o usuário componha a maior parte do
conteúdo. Abordagens assistidas por IA mais recentes (MeetingVis, NoTeeline, GazeNoter)
mostram como LLMs e interação multimodal podem expandir entradas curtas em notas ricas,
reduzindo esforço cognitivo.

**Gestão de conhecimento pessoal (PKM) e roteamento.** Ferramentas de PKM estruturam notas
heterogêneas do usuário em entidades organizadas, permitindo fluxos de recuperação e sugestão.
O roteamento automático de notas para tipos semânticos é paralelo à classificação de intenção
e à marcação (tagging) em sistemas de anotação. Abordagens anteriores costumam usar pipelines
de prompt com LLM para marcação — precisos, mas com alta latência, custo e preocupações de
privacidade para dados sensíveis. Modelos só-codificador (encoder-only) oferecem alternativa
prática, sustentando implantação eficiente em dispositivo ou baseada em CPU.

**Classificação multi-rótulo de notas.** Atribui múltiplos rótulos semânticos a uma única
nota, refletindo intenções sobrepostas e funções diversas. Notas curtas e informais costumam
conter múltiplas intenções entrelaçadas, o que torna a classificação multi-rótulo
particularmente adequada. Transformers só-codificador como BERT e DeBERTa oferecem
representações eficazes em nível de sentença e continuam sendo baselines fortes. O DeBERTa-v3
introduz atenção desemaranhada (disentangled attention) e sinais de pré-treino aprimorados que
melhoram a qualidade de classificação sem adicionar complexidade de inferência.

## III. NoteBar

### A. Princípios de design

O design do NoteBar é guiado pela necessidade de conectar os benefícios cognitivos da
anotação tradicional com a escalabilidade e eficiência de sistemas assistidos por IA. Três
princípios centrais:

**Condicionamento por persona para desambiguação.** Suporte eficaz à anotação exige
sensibilidade à variação individual de estilo de escrita, intenção e papel. Informação de
persona pode ser usada para desambiguar enunciados que de outra forma pareceriam similares.
O condicionamento por persona normaliza frases ruidosas ou idiossincráticas em representações
mais simples e limpas que destacam limites de conceito — conceitos semanticamente distintos
que poderiam parecer confundidos no texto bruto da nota podem ser roteados de forma mais
confiável para categorias diferentes.

**Roteamento multi-rótulo com transformers eficientes.** Notas frequentemente expressam
múltiplos conceitos simultaneamente (ex.: #tarefa, #insight, #ideia), tornando a classificação
multi-rótulo essencial. O NoteBar formula o roteamento como um problema de classificação
multi-rótulo e usa transformers só-codificador (ex.: DeBERTa-v3) como espinha dorsal,
equilibrando qualidade de tarefa com implantabilidade via quantização e serviço priorizando
CPU.

**Feedback com humano no ciclo (user-in-the-loop) para robustez.** Classificação automática
sozinha não captura totalmente a intenção do usuário. O NoteBar é desenhado para incorporar um
ciclo de feedback onde o usuário pode aceitar, rejeitar ou editar sugestões do sistema.
Embora essa funcionalidade ainda não esteja implementada na versão atual, representa um
componente importante do design e área ativa de desenvolvimento.

### B. Arquitetura do sistema

A arquitetura do NoteBar é um pipeline modular que conecta captura de nota, classificação,
recuperação e, eventualmente, feedback. Quando o usuário cria uma nota no app, a entrada é
armazenada num banco de dados não-relacional junto com metadado contextual (timestamp,
dispositivo). Um classificador baseado em BERT é aplicado a esse conteúdo, realizando
roteamento multi-rótulo que atribui cada nota a um ou mais tipos semânticos.

Para sustentar sugestões via recuperação aumentada, notas processadas são embutidas
(embedded) e armazenadas num banco de dados vetorial, permitindo busca por similaridade
semântica. Um orquestrador RAG (geração aumentada por recuperação) usa esse índice para montar
informação contextual e produzir sugestões candidatas — como linkar uma nota a um evento de
calendário, playbook ou tarefa kanban. Itens acionáveis como prazos podem ser sincronizados
automaticamente com o calendário do usuário.

### C. Detalhes de implementação

Notas são armazenadas primeiro num banco não-relacional (Firebase Firestore) para dar suporte
flexível de schema a entradas heterogêneas do usuário. Para classificação, adota-se uma
arquitetura transformer só-codificador: um backbone DeBERTa-v3-base é treinado para
roteamento multi-rótulo, usando AdamW com aquecimento linear de taxa de aprendizado (learning
rate) de 2×10⁻⁵ e batch size de 8, atingindo convergência estável em 10 épocas. O banco de
dados vetorial é implementado com Pinecone.

## IV. Experimentos e Avaliação

### A. Dataset

Recursos existentes para avaliar sistemas de anotação e fluxos de PKM são limitados. Para
resolver essa lacuna, os autores construíram um dataset sintético via pipeline automatizado
baseado em agentes, projetado para simular comportamento realista de anotação, mantendo
consistência estrutural e fidelidade semântica.

O pipeline de geração de dados tem quatro estágios, usando GPT-4o como modelo de linguagem
subjacente:

1. **Agente de Persona (geração de nota):** cada persona é definida por um perfil estruturado
   baseado nos 16 tipos do Myers-Briggs (MBTI), com prompts contextuais especificando rotina
   diária, interesses e estilo de escrita. Cada persona segue um plano de oito semanas para
   simular continuidade temporal.
2. **Roteador de Conceito (extração de conteúdo):** processa as notas geradas, transformando
   texto livre em anotações JSON estruturadas — tipo de nota, entidades, estados cognitivos, e
   atribuição a uma taxonomia predefinida de tipos (tarefa, insight, ideia). Cada conceito é
   enriquecido com análise em cinco dimensões retóricas (telos, logos, ethos, pathos, kairos).
3. **Agente de QA de Anotação (validação e refinamento):** procedimento de garantia de
   qualidade em dois estágios — verificações baseadas em regra (schema, tipo, faixa numérica)
   e verificações baseadas em LLM (consistência de escore canônico, plausibilidade semântica),
   com mecanismo de correção automática para problemas críticos.
4. **Sugestões do NoteBar (opcional):** notas processadas podem ser linkadas a artefatos como
   eventos de calendário, playbooks e tarefas kanban.

### B. Estatísticas do dataset

O dataset final contém 3.173 notas e 8.494 anotações de conceito em 16 personas, das quais
8.349 conceitos passaram na validação de QA. Em média, cada nota está associada a 2,7
conceitos. O dataset é dominado pela categoria "tarefa" (5.170 instâncias), seguida de
"insight" (1.209) e "ideia" (650), enquanto categorias raras como "solução", "ação de UI" e
"comunicação" aparecem só uma vez — distribuição de cauda longa que espelha cenários reais de
PKM.

### C. Configuração experimental e resultados

Foram testados três backbones: `bert-base-uncased` (baseline), `roberta-base` e
`deberta-v3-base`. O DeBERTa-v3-base superou claramente as alternativas, alcançando Acurácia
de 0,78 e F1 de 0,76. BERT teve desempenho moderado, e RoBERTa o resultado mais fraco (Acc:
0,69, F1: 0,61) — a lacuna de desempenho destaca a efetividade da atenção desemaranhada e do
pré-treino aprimorado do DeBERTa para discriminar tipos semânticos sobrepostos.

**Sensibilidade a hiperparâmetro:** batch size menor (8) rendeu resultados consistentemente
mais fortes que batches maiores. Taxa de aprendizado moderada (2×10⁻⁵) produziu a melhor
Acurácia (0,775) e F1 (0,757) — taxas maiores degradaram ou desestabilizaram o treino. O
desempenho melhorou de forma estável até ~10 épocas, depois disso os ganhos diminuem e surge
leve overfitting.

## V. Limitações e Planos Futuros

**Limitações:** a taxonomia de 20 tipos semânticos, embora cubra fluxos comuns de PKM, não é
exaustiva — contextos específicos de domínio (notas de programação, citações de pesquisa,
anotações de UI) ficam fora do escopo. O sistema assume entrada em inglês, deixando a anotação
multilíngue sem tratamento. O dataset tem distribuição de cauda longa: categorias raras são
severamente sub-representadas. A geração sintética de dados, embora permita cobertura ampla e
controlabilidade, arrisca reforçar padrões templatizados e pode divergir de comportamento real
de usuário. O condicionamento por persona, embora melhore a separabilidade de rótulo, também
pode introduzir correlações espúrias entre estilo de persona e distribuição de rótulo.

**Planos futuros:** expandir a taxonomia para tipos de nota específicos de domínio, estender
avaliação a contextos multilíngues, explorar active learning e calibração por rótulo para o
problema de cauda longa, suplementar gradualmente o treino com notas reais de usuário (opt-in,
preservando privacidade), conduzir auditorias sistemáticas de equidade, e completar o design
do módulo de feedback com humano no ciclo.

## VI. Conclusão

Apresentamos o NoteBar, um framework só-codificador guiado por persona para roteamento
multi-rótulo de conceito em gestão de conhecimento pessoal. Usando um dataset sintético de 16
personas (3.173 notas; 8.494 conceitos anotados), demonstramos que geração de dados controlada
e pipelines de QA sustentam classificação confiável. O DeBERTa-v3-base atinge desempenho forte
nessa tarefa desafiadora de cauda longa, oferecendo ganhos de eficiência significativos sobre
heurísticas baseadas em GPT. Ao mesmo tempo, várias limitações permanecem: taxonomia
restrita, desempenho em rótulo raro, deriva potencial em dado sintético, e riscos de equidade
do condicionamento por persona. O módulo de feedback com humano no ciclo ainda não foi
implementado e será prioridade em trabalho futuro.

## Agradecimentos

Os autores agradecem os mantenedores do BERT, do ecossistema Hugging Face Transformers e do
LangChain. Pesquisa financiada com créditos de nuvem do Google Cloud for Startups, com apoio
do NYS Center of Excellence — Goergen Institute for Data Science and AI, e do Skidmore College
Summer Experience Fund. A API da OpenAI foi usada para processamento e geração de texto durante
o desenvolvimento do modelo. Todos os datasets usados neste estudo foram criados pelos autores.

---

*Lista de referências bibliográficas (39 itens), figuras, tabelas de resultado numérico e
apêndices adicionais mantidos apenas no arquivo original em inglês —
`wisoff-et-al-notebar-ai-note-taking-pkm.pdf`.*
