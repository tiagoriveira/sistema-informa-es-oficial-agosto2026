---
tipo: conceito
disciplina: product-discovery
titulo: Over-serving e job mal atendido
fontes: []
criado: 2026-08-18
atualizado: 2026-08-18
---

# Over-serving e job mal atendido

**Ideia central:** um produto pode "atender demais" numa dimensão que o cliente já achava
suficiente, enquanto deixa mal atendida a dimensão que realmente decide a contratação — o
cliente não larga o produto, mas o contrata por resignação, sem alternativa melhor.

## Explicação
Extensão da teoria da disrupção de Christensen sobre [[jobs-to-be-done]]: nem todo cliente que
usa um produto está satisfeito com o job que ele resolve. Às vezes a empresa empilha
funcionalidade numa dimensão que o cliente já considera "boa o suficiente" (ex.: mais recursos
financeiros avançados), enquanto a dimensão que realmente pesa pro job dele (ex.: simplicidade,
zero curva de aprendizado) continua mal resolvida. O resultado é **contratação por resignação**:
o cliente usa o produto, mas incompletamente, e mantém um workaround paralelo pra cobrir o que
o produto devia resolver sozinho.

Isso é diferente de "produto ruim" — o produto pode ser tecnicamente excelente na dimensão
errada. O diagnóstico não é "o que falta", é "em qual dimensão o cliente está sendo mal servido
apesar de já pagar por algo".

## Sinais de job mal atendido
- Uso baixo de funcionalidades pagas — paga pelo pacote completo, usa uma fração dele.
- Workaround paralelo — planilha, contador ou processo manual rodando junto do produto, não
  substituído por ele.
- Linguagem recorrente de frustração em texto público: "não uso metade disso", "é complicado
  demais", "preciso de ajuda toda vez que mexo".
- Retenção alta combinada com satisfação baixa — sintoma de "não tenho opção melhor", não de
  "gosto do produto".

## Como pesquisar isso com IA
[[ia-pesquisa-posicionamento-concorrencia]] já descreve o mecanismo de social listening — IA
agrupando queixa/desejo recorrente em padrão. O mesmo mecanismo, apontado pra dentro (a própria
categoria de produto, não só concorrente), serve pra achar over-serving: minerar review de app,
Reclame Aqui, fórum e comentário de vídeo em busca de cluster de queixa por dimensão do job
(simplicidade vs. completude de recurso, confiança, tempo gasto).

**Limite importante:** isso gera hipótese, não confirmação. Padrão de texto público mostra
onde procurar, mas não confirma o que o cliente faria de fato — fechar o ciclo exige entrevista
sobre comportamento passado (item 9 da Fase 3 de [[mapa-product-discovery]], ainda não
estudado). Tratar cluster de review como prova validada seria inventar evidência que a pesquisa
ainda não deu.

## Exemplo
Software de gestão financeira pra produtor rural: complexo, com recursos avançados de fluxo de
caixa e relatório, mas o job real do produtor é "manter as finanças organizadas sem precisar
entender de finanças e sem perder tempo" (mesmo exemplo-base de [[jobs-to-be-done]]). Se o
software over-serve em recurso avançado e under-serve em simplicidade, o produtor paga a
licença **e** mantém o contador em paralelo — o software foi contratado, mas por resignação,
não porque resolveu o job sozinho. O gap de mercado aqui não é "mais recurso", é uma versão
radicalmente mais simples, mesmo que com menos funcionalidade.

## Relacionado
[[jobs-to-be-done]] · [[ia-pesquisa-posicionamento-concorrencia]] · [[validacao-de-problema]]

## Conhecimento externo (fora das suas fontes)
> Esta disciplina não tem fontes em `RAW/`. Conceito de over-serving vem da teoria da disrupção
> de Clayton Christensen (extensão de JTBD), trazido por conhecimento externo da IA, não de uma
> fonte ingerida — ver `CLAUDE.md` §6.
