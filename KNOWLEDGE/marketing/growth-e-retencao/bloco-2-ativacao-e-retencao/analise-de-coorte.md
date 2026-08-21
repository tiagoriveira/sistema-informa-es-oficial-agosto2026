---
tipo: conceito
disciplina: growth-e-retencao
titulo: Análise de coorte: separar quem entrou junto para ver o que a média esconde
fontes: []
criado: 2026-08-20
atualizado: 2026-08-20
---

# Análise de coorte: separar quem entrou junto para ver o que a média esconde

**Ideia central:** agrupar usuários pelo momento em que entraram e acompanhar cada grupo ao
longo do tempo — é o que permite distinguir "o produto melhorou" de "entrou mais gente".

## O mecanismo
Uma tabela: cada linha é um grupo de entrada (mês, semana, campanha), cada coluna é o tempo
decorrido desde a entrada. A célula mostra quantos ainda estão ativos.

Três leituras que só aparecem assim:
- **A curva achata?** Se cai e estabiliza, existe um núcleo para quem o produto serve. Se cai
  até o fim, não existe.
- **Coorte nova é melhor que antiga?** É a única prova de que uma mudança de produto funcionou.
- **A origem muda a curva?** Cliente vindo de indicação costuma reter diferente de cliente vindo
  de anúncio — e isso muda quanto vale pagar por cada um.

## Exemplo
A métrica agregada de usuários ativos sobe três meses seguidos e a diretoria comemora. Por
coorte, cada grupo novo retém pior que o anterior: o total sobe porque a aquisição cresceu, e o
produto está piorando. A média escondia exatamente o que importava.

## Aplicação
Toda vez que um número agregado mudar, pergunte **qual coorte mudou**. É o antídoto direto ao
efeito descrito em [[mapa-estatistica-para-decisao-marketing]] Fase 1: média que esconde a
distribuição.

## Erros comuns
- Comparar coortes com tempos de vida diferentes.
- Coorte pequena demais — a variação é ruído.
- Definir a coorte por data de cadastro quando o que importa é data de ativação.

## Relacionado
[[iceberg-da-retencao]] · [[north-star-metric]] · [[churn-preditivo]]

## Conhecimento externo (fora das suas fontes)
> Não está em nenhuma fonte do `RAW/`. Mecanismo estável, sem número de referência —
> os benchmarks que circulam nesta área vêm de amostras de empresas financiadas por
> capital de risco e não transferem para outro contexto.
