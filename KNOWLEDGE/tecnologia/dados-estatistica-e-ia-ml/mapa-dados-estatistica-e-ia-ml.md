---
tipo: mapa
disciplina: dados-estatistica-e-ia-ml
hub: tecnologia
atualizado: 2026-08-17
---

# Mapa — Dados, Estatística e IA/ML

**Fontes desta disciplina:** nenhuma em `RAW/` — grade checada por busca na web em 2026-08-17
(ver "Nota sobre a grade").
**Estado do aluno:** [[estado-dados-estatistica-e-ia-ml]]

**Pré-requisito:** [[mapa-fundamentos-de-programacao]]. **Fronteira com
[[mapa-colaboracao-humano-ia]]** (hub inteligencia-artificial): aqui é a técnica por trás do
modelo (estatística, treino, arquitetura); lá é como humano e IA dividem trabalho no uso do
dia a dia — este mapa é o "como funciona por dentro", aquele é o "como colaborar bem".
**Fronteira também com [[mapa-arquitetura-de-agentes-e-contexto]]** (mesmo hub que
colaboracao-humano-ia): a Fase 5 aqui (orquestração, IA agêntica) é onde este mapa termina —
aquele mapa aprofunda o assunto na camada de arquitetura de arquivo/pasta/skill, agnóstica de
framework específico.

**Fronteira com [[mapa-estatistica-para-decisao-marketing]]:** em 2026-08-20, os fundamentos de
estatística conceitual (descritiva, probabilidade, inferência — sem SQL nem código) foram
separados pra essa disciplina nova, com sabor de decisão de negócio/marketing, não de
ciência de dados. Esta disciplina aqui fica só com o que é genuinamente técnico: manipulação de
dado, ML, deep learning, agentes (Fases 2-5). Se um dia isso for estudado a fundo, os itens 1-3
da Fase 1 abaixo apontam pra lá em vez de reensinar o mesmo conceito.

## Ordem de estudo sugerida
_(status derivado do LEARNER — não editar à mão, regenerado a cada UPDATE. `CLAUDE.md` §4.2:
esta ordem não é dogma, desvie quando houver motivo)_

### Fase 1 — Estatística e matemática aplicada
1. _(movido para [[mapa-estatistica-para-decisao-marketing]] em 2026-08-20 — ver item 1 de lá)_
2. _(movido para [[mapa-estatistica-para-decisao-marketing]] — ver item 5 de lá)_
3. _(movido para [[mapa-estatistica-para-decisao-marketing]] — ver itens 9-12 de lá)_
4. ⬜ Álgebra linear e cálculo aplicados — o que o ML usa de verdade (fica aqui: é matemática de
   ML, não estatística de decisão)

### Fase 2 — Manipulação e análise de dados
5. ⬜ Coleta e limpeza de dado — o trabalho que decide o resultado
6. ⬜ SQL e consulta de dado
7. ⬜ Análise exploratória e visualização
8. ⬜ Viés e qualidade de dado — por que o resultado pode estar errado antes do modelo

### Fase 3 — Machine learning, fundamentos
9. ⬜ Aprendizado supervisionado vs. não-supervisionado
10. ⬜ Regressão e classificação — os dois problemas básicos
11. ⬜ Overfitting e underfitting — o modelo decorou ou aprendeu
12. ⬜ Métrica de avaliação — acurácia não basta
13. ⬜ Árvore de decisão e ensemble (random forest, boosting)

### Fase 4 — Deep learning e IA generativa
14. ⬜ Redes neurais — a ideia por trás do deep learning
15. ⬜ Como um LLM funciona — de token a resposta
16. ⬜ Prompt engineering — como pedir certo pro modelo
17. ⬜ RAG — conectar LLM a conhecimento externo
18. ⬜ Fine-tuning vs. RAG vs. prompt — quando usar cada abordagem

### Fase 5 — IA aplicada e agentes
19. ⬜ Orquestração e frameworks (ex.: LangChain) — encadear chamada de IA
20. ⬜ IA agêntica — quando o modelo decide a próxima ação sozinho
21. ⬜ Avaliação de sistema de IA — como saber se está funcionando de verdade
22. ⬜ Ética, viés e limite — o que a IA não deve decidir sozinha

## Nota sobre a grade
Grade desenhada em 2026-08-17 a partir de busca na web (regra `CLAUDE.md` §6). Área que
envelhece rápido — Fases 4 e 5 (IA generativa, agentes) são as que mais mudam e precisam de
recheck antes de estudar, não assunção. Fases 1-3 (estatística, dado, ML clássico) são estáveis.

**Débito conhecido (2026-08-20):** Fase 1 ficou com só 1 item ativo depois da migração pra
[[mapa-estatistica-para-decisao-marketing]] — abaixo do mínimo de 4-6 do `schema.md` §3. Não
fundida com a Fase 2 agora pra evitar renumerar a grade inteira sem necessidade real (nada
avaliado ainda, risco baixo de deixar como está). Fica como item de `LINT` futuro.

**Fontes consultadas:**
- [The Ultimate Data Science Roadmap 2026 — 365 Data Science](https://365datascience.com/career-advice/career-guides/data-science-roadmap/)
- [Data Science Roadmap 2026 — DataCamp](https://www.datacamp.com/blog/data-science-roadmap)
- [Machine Learning Roadmap for 2026 — Scaler](https://www.scaler.com/blog/machine-learning-roadmap/)
