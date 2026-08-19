---
fonte_original: xu-et-al-a-mem-agentic-memory-llm-agents.pdf
traduzido_por: ia
traduzido_em: 2026-08-18
nota: >
  Tradução do corpo científico do paper (arXiv 2502.12110, aceito no NeurIPS 2025). Fórmulas
  matemáticas mantidas em notação original. Templates de prompt (Apêndice B) mantidos em
  inglês — são o artefato literal usado pelo sistema, traduzir mudaria o que o sistema
  realmente executa. Checklist de ética do NeurIPS (formalidade de submissão, não conteúdo
  científico) e tabelas numéricas completas do apêndice omitidas — ver original em inglês.
---

# A-MEM: Memória Agêntica para Agentes de LLM

**Autores:** Wujiang Xu¹, Zujie Liang², Kai Mei¹, Hang Gao¹, Juntao Tan¹, Yongfeng Zhang¹˒³
¹Rutgers University · ²Pesquisador Independente · ³AIOS Foundation

## Resumo

Embora agentes de modelo de linguagem de larga escala (LLM) possam usar ferramentas externas
de forma eficaz para tarefas complexas do mundo real, eles precisam de sistemas de memória
para aproveitar experiências históricas. Sistemas de memória atuais permitem armazenamento e
recuperação básicos, mas carecem de organização de memória sofisticada, apesar de tentativas
recentes de incorporar bancos de dados de grafo. Além disso, as operações e estruturas fixas
desses sistemas limitam sua adaptabilidade em tarefas diversas. Para resolver essa limitação,
este paper propõe um sistema de memória agêntica inédito para agentes de LLM que consegue
organizar memórias dinamicamente, de forma agêntica. Seguindo os princípios básicos do método
Zettelkasten, desenhamos nosso sistema de memória para criar redes de conhecimento
interconectadas através de indexação e linkagem dinâmicas. Quando uma nova memória é
adicionada, geramos uma nota abrangente contendo múltiplos atributos estruturados, incluindo
descrições contextuais, palavras-chave e tags. O sistema então analisa memórias históricas
para identificar conexões relevantes, estabelecendo links onde existem similaridades
significativas. Além disso, esse processo permite evolução de memória — conforme novas
memórias são integradas, elas podem disparar atualizações nas representações contextuais e
atributos de memórias históricas existentes, permitindo que a rede de memória refine
continuamente sua compreensão. Nossa abordagem combina os princípios de organização
estruturada do Zettelkasten com a flexibilidade da tomada de decisão guiada por agente,
permitindo gestão de memória mais adaptativa e sensível a contexto. Experimentos empíricos em
seis modelos de fundação mostram melhoria superior contra baselines estado-da-arte existentes.

## 1. Introdução

Agentes de LLM demonstraram capacidades notáveis em várias tarefas, com avanços recentes
permitindo que interajam com ambientes, executem tarefas e tomem decisões de forma autônoma.
Eles integram LLMs com ferramentas externas e fluxos de trabalho delicados para melhorar
raciocínio e planejamento. Embora o agente de LLM tenha forte desempenho de raciocínio, ele
ainda precisa de um sistema de memória para fornecer capacidade de interação de longo prazo
com o ambiente externo.

Sistemas de memória existentes para agentes de LLM fornecem funcionalidade básica de
armazenamento de memória. Esses sistemas exigem que desenvolvedores de agente predefinam
estruturas de armazenamento de memória, especifiquem pontos de armazenamento dentro do fluxo
de trabalho e estabeleçam o timing de recuperação. Enquanto isso, para melhorar a organização
estruturada de memória, o Mem0, seguindo os princípios do RAG, incorpora bancos de dados de
grafo para os processos de armazenamento e recuperação. Embora bancos de dados de grafo
forneçam organização estruturada para sistemas de memória, sua dependência de esquemas e
relacionamentos predefinidos limita fundamentalmente sua adaptabilidade. Essa limitação se
manifesta claramente em cenários práticos — quando um agente aprende uma solução matemática
nova, sistemas atuais só conseguem categorizar e linkar essa informação dentro do framework
preestabelecido, incapazes de forjar conexões inovadoras ou desenvolver novos padrões
organizacionais conforme o conhecimento evolui.

Neste paper, introduzimos um sistema de memória agêntica inédito, chamado A-MEM, para agentes
de LLM, que permite estruturação dinâmica de memória sem depender de operações de memória
estáticas e predeterminadas. Nossa abordagem se inspira no método Zettelkasten, um sistema
sofisticado de gestão de conhecimento que cria redes de informação interconectadas através de
notas atômicas e mecanismos de linkagem flexíveis. Nosso sistema introduz uma arquitetura de
memória agêntica que permite gestão de memória autônoma e flexível para agentes de LLM. Para
cada nova memória, construímos notas abrangentes, que integram múltiplas representações:
atributos textuais estruturados incluindo vários atributos e vetores de embedding para
correspondência de similaridade. Então o A-MEM analisa o repositório de memória histórica para
estabelecer conexões significativas baseadas em similaridades semânticas e atributos
compartilhados. Esse processo de integração não só cria novos links, mas também permite
evolução dinâmica — quando novas memórias são incorporadas, elas podem disparar atualizações
nas representações contextuais de memórias existentes, permitindo que toda a memória refine e
aprofunde continuamente sua compreensão ao longo do tempo.

**Contribuições:**
- Apresentamos o A-MEM, um sistema de memória agêntica para agentes de LLM que permite geração
  autônoma de descrições contextuais, estabelecimento dinâmico de conexões de memória, e
  evolução inteligente de memórias existentes baseada em novas experiências.
- Desenhamos um mecanismo de atualização de memória agêntica onde novas memórias disparam
  automaticamente duas operações-chave: geração de link e evolução de memória.
- Conduzimos avaliações abrangentes usando um dataset conversacional de longo prazo, comparando
  desempenho em seis modelos de fundação usando seis métricas de avaliação distintas,
  demonstrando melhorias significativas.

## 2. Trabalhos Relacionados

**Memória para agentes de LLM.** Trabalhos anteriores exploraram vários mecanismos de gestão e
uso de memória. Algumas abordagens completam o armazenamento de interação via modelos de
recuperação densa ou estruturas de leitura-escrita. O MemGPT usa arquiteturas tipo cache para
priorizar informação recente. O SCM propõe um framework de Memória Autocontrolada que aprimora
a capacidade dos LLMs de manter memória de longo prazo através de um fluxo de memória e
mecanismo controlador. No entanto, essas abordagens enfrentam limitações significativas ao
lidar com tarefas diversas do mundo real — suas operações são tipicamente restringidas por
estruturas predefinidas e fluxos de trabalho fixos.

**Geração aumentada por recuperação (RAG).** O RAG surgiu como abordagem poderosa para
aprimorar LLMs incorporando fontes de conhecimento externas. O processo RAG padrão envolve
indexar documentos em blocos, recuperar blocos relevantes baseado em similaridade semântica, e
aumentar o prompt do LLM com esse contexto recuperado para geração. Sistemas RAG avançados
evoluíram para incluir otimizações sofisticadas de pré e pós-recuperação. Diferente das
abordagens de RAG agêntico, que demonstram agência na fase de recuperação decidindo
autonomamente quando e o que recuperar, nosso sistema de memória agêntica exibe agência num
nível mais fundamental através da evolução autônoma de sua estrutura de memória.

## 3. Metodologia

### 3.1 Construção de nota

Construindo sobre os princípios de anotação atômica e organização flexível do método
Zettelkasten, introduzimos uma abordagem guiada por LLM para construção de nota de memória.
Quando um agente interage com seu ambiente, construímos notas de memória estruturadas que
capturam tanto informação explícita quanto compreensão contextual gerada por LLM. Cada nota de
memória mᵢ em nossa coleção é representada como:

`mᵢ = {cᵢ, tᵢ, Kᵢ, Gᵢ, Xᵢ, eᵢ, Lᵢ}`

onde cᵢ representa o conteúdo original da interação, tᵢ é o timestamp, Kᵢ denota
palavras-chave geradas por LLM que capturam conceitos-chave, Gᵢ contém tags geradas por LLM
para categorização, Xᵢ representa a descrição contextual gerada por LLM, e Lᵢ mantém o
conjunto de memórias linkadas que compartilham relações semânticas. Seguindo o princípio de
atomicidade do Zettelkasten, cada nota captura uma unidade única e autocontida de conhecimento.

### 3.2 Geração de link

O sistema implementa um mecanismo autônomo de geração de link que permite que novas notas de
memória formem conexões significativas sem regras predefinidas. Quando a nota de memória mₙ é
adicionada ao sistema, primeiro usamos seu embedding semântico para recuperação baseada em
similaridade, calculando um escore de similaridade (similaridade de cosseno) entre mₙ e cada
memória existente. O sistema então identifica as k memórias mais relevantes e solicita ao LLM
que analise conexões potenciais baseadas em seus atributos comuns potenciais. O uso de
recuperação baseada em embedding como filtro inicial permite escalabilidade eficiente mantendo
relevância semântica — mais importante, a análise guiada por LLM permite compreensão
sutil de relacionamentos que vai além de métricas simples de similaridade, identificando
padrões sutis, relações causais e conexões conceituais que poderiam não ser aparentes só pela
similaridade de embedding.

### 3.3 Evolução de memória

Depois de criar links para a nova memória, o A-MEM evolui as memórias recuperadas baseado em
sua informação textual e relações com a nova memória. Para cada memória mⱼ no conjunto de
vizinhos mais próximos, o sistema determina se deve atualizar seu contexto, palavras-chave e
tags. A memória evoluída substitui a memória original no conjunto de memória. Essa abordagem
evolutiva permite atualizações contínuas e novas conexões, imitando processos de aprendizado
humano. Conforme o sistema processa mais memórias ao longo do tempo, desenvolve estruturas de
conhecimento cada vez mais sofisticadas, descobrindo padrões e conceitos de ordem superior
entre múltiplas memórias.

### 3.4 Recuperar memória relativa

Em cada interação, o A-MEM realiza recuperação de memória sensível a contexto para fornecer ao
agente informação histórica relevante. Dado um texto de consulta da interação atual, o sistema
calcula sua representação vetorial densa usando o mesmo codificador de texto usado para as
notas de memória, computa escores de similaridade entre o embedding de consulta e todas as
notas de memória existentes, e recupera as k memórias mais relevantes para construir um prompt
contextualmente apropriado.

## 4. Experimentos

Para avaliar a efetividade em conversas de longo prazo, os autores usam o dataset LoCoMo, que
contém diálogos significativamente mais longos que datasets conversacionais existentes (~9 mil
tokens em até 35 sessões, contra ~1 mil tokens em 4-5 sessões de datasets anteriores). O LoCoMo
tem cinco tipos de pergunta: single-hop, multi-hop, raciocínio temporal, conhecimento de
domínio aberto, e perguntas adversariais (não-respondíveis) — 7.512 pares pergunta-resposta no
total. Também é usado o DialSim, dataset de perguntas e respostas derivado de diálogos
multi-parte de longo prazo (séries de TV: Friends, The Big Bang Theory, The Office — 1.300
sessões ao longo de cinco anos, ~350 mil tokens).

Baselines de comparação: LoCoMo (usa a conversa completa no prompt, sem mecanismo de memória),
ReadAgent (paginação de episódio + resumo em "gist" + busca interativa), MemoryBank (curva de
esquecimento de Ebbinghaus para força de memória), MemGPT (hierarquia de memória inspirada em
sistema operacional, com contexto principal tipo RAM e contexto externo tipo disco).

**Resultados principais:** para modelos que não são GPT, o A-MEM supera consistentemente todos
os baselines em todas as categorias. Para modelos baseados em GPT, enquanto LoCoMo e MemGPT
mostram desempenho forte em certas categorias (Domínio Aberto, Adversarial) devido ao seu
conhecimento pré-treinado robusto para recuperação simples de fato, o A-MEM demonstra
desempenho superior em tarefas Multi-Hop, alcançando pelo menos o dobro de desempenho em
tarefas que exigem cadeias de raciocínio complexas. No dataset DialSim, o A-MEM supera todos
os baselines em todas as métricas de avaliação, alcançando escore F1 de 3,45 (melhoria de 35%
sobre o 2,55 do LoCoMo e 192% maior que o 1,18 do MemGPT).

**Eficiência de custo:** o A-MEM requer aproximadamente 1.200 tokens por operação de memória,
alcançando redução de 85-93% no uso de token comparado aos métodos baseline (LoCoMo e MemGPT
com 16.900 tokens) através do mecanismo seletivo de recuperação top-k. Essa redução substancial
de token se traduz diretamente em custo operacional menor, com cada operação de memória
custando menos de $0,0003 usando serviços de API comerciais — viabilizando economicamente
implantações em larga escala.

**Estudo de ablação:** quando os módulos de Geração de Link (LG) e Evolução de Memória (ME)
são removidos, o sistema exibe degradação substancial de desempenho, particularmente em
raciocínio Multi-Hop e tarefas de Domínio Aberto. O modelo completo A-MEM consistentemente
alcança o melhor desempenho em todas as categorias avaliadas, revelando que, enquanto o módulo
de geração de link serve como fundação crítica para organização de memória, o módulo de
evolução de memória fornece refinamentos essenciais à estrutura de memória.

**Análise de escala:** em termos de complexidade espacial, os três sistemas testados exibem
escala de uso de memória linear idêntica — o A-MEM não introduz overhead adicional de
armazenamento comparado a abordagens baseline. Para tempo de recuperação, mesmo escalando para
1 milhão de memórias, o tempo de recuperação do A-MEM aumenta só de 0,31µs para 3,70µs.

## 5. Conclusões

Neste trabalho, introduzimos o A-MEM, um sistema de memória agêntica inédito que permite a
agentes de LLM organizar e evoluir suas memórias dinamicamente, sem depender de estruturas
predefinidas. Inspirando-se no método Zettelkasten, nosso sistema cria uma rede de
conhecimento interconectada através de mecanismos dinâmicos de indexação e linkagem que se
adaptam a tarefas diversas do mundo real. A arquitetura central do sistema apresenta geração
autônoma de descrições contextuais para novas memórias e estabelecimento inteligente de
conexões com memórias existentes baseado em atributos compartilhados. Além disso, nossa
abordagem permite evolução contínua de memórias históricas ao incorporar novas experiências e
desenvolver atributos de ordem superior através de interações contínuas.

## 6. Limitações

Embora nosso sistema de memória agêntica alcance resultados promissores, reconhecemos várias
áreas para exploração futura potencial. Primeiro, embora nosso sistema organize memórias
dinamicamente, a qualidade dessas organizações ainda pode ser influenciada pelas capacidades
inerentes dos modelos de linguagem subjacentes — LLMs diferentes podem gerar descrições
contextuais ligeiramente diferentes ou estabelecer conexões variadas entre memórias.
Adicionalmente, embora nossa implementação atual foque em interações baseadas em texto,
trabalho futuro poderia explorar estender o sistema para lidar com informação multimodal, como
imagens ou áudio, que poderia fornecer representações contextuais mais ricas.

---

*Lista de referências bibliográficas (39 itens), templates de prompt (Apêndice B — mantidos
em inglês por serem o artefato literal do sistema), tabelas numéricas completas de todos os
experimentos e o checklist de ética do NeurIPS mantidos apenas no arquivo original em inglês —
`xu-et-al-a-mem-agentic-memory-llm-agents.pdf`.*
