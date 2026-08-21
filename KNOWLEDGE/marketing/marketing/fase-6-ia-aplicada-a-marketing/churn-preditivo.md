---
tipo: conceito
disciplina: marketing
titulo: Churn preditivo: prever quem vai sair enquanto ainda dá para agir
fontes: []
criado: 2026-08-20
atualizado: 2026-08-20
---

# Churn preditivo: prever quem vai sair enquanto ainda dá para agir

**Ideia central:** um modelo estima a probabilidade de cada cliente cancelar a partir do
comportamento recente — e o valor não está na previsão, está em **existir uma ação diferente**
para quem foi marcado como risco.

## O mecanismo
- **Sinal.** Comportamento (queda de uso, redução de frequência, chamado de suporte, atraso de
  pagamento) prevê melhor do que perfil demográfico.
- **Separação que dobra a utilidade.** Saída voluntária (a pessoa decidiu sair) e involuntária
  (cartão recusado, falha de cobrança) exigem ações completamente diferentes — e misturar as
  duas no mesmo modelo estraga as duas.
- **Faixa de risco ligada a gatilho.** O modelo entrega uma nota; a operação precisa dizer o que
  acontece em cada faixa. Sem isso, você comprou um relatório.

## Exemplo
Um modelo aponta 200 clientes em risco alto. Sem plano, a lista circula e nada muda. Com plano —
faixa alta vai para contato humano, faixa média para oferta de ajuda, involuntária para
atualização de pagamento —, a mesma lista vira retenção.

## Aplicação
Comece sem modelo: defina dois ou três sinais de risco por regra simples e monte a ação. Se a
ação funcionar na regra, o modelo depois melhora a precisão. Se não funcionar, o modelo não vai
salvar.

## Erros comuns
- Construir o modelo antes de definir a intervenção.
- Confundir correlação com causa e "tratar" um sintoma — ver
  [[mapa-estatistica-para-decisao-marketing]] Fase 2.
- Oferecer desconto a quem ia ficar, o que destrói margem sem reter ninguém.
- Não medir contra grupo de controle e concluir que a ação funcionou.

## Relacionado
[[iceberg-da-retencao]] · [[analise-de-coorte]] · [[first-party-data]]

## Conhecimento externo (fora das suas fontes)
> Checado por busca na web em 2026-08-20 — predominância de variável comportamental sobre
> demográfica e a separação entre saída voluntária e involuntária como prática corrente. Fonte:
> [Digital Applied](https://www.digitalapplied.com/blog/customer-churn-prediction-models-marketing-framework-2026).
> Ganhos de acurácia e escolha de algoritmo citados por essa fonte não foram transcritos como fato.
