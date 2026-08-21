---
tipo: conceito
disciplina: marketing-tecnico
titulo: Analytics de evento: quando a página deixou de ser a unidade de medida
fontes: []
criado: 2026-08-20
atualizado: 2026-08-20
---

# Analytics de evento: quando a página deixou de ser a unidade de medida

**Ideia central:** o modelo antigo contava visitas a páginas; o modelo de evento conta **ações
com parâmetros**, o que permite medir produto e funil, mas exige que alguém defina antes o que
é uma ação relevante.

## O mecanismo
Tudo é evento: ver tela, rolar, clicar, comprar. Cada evento carrega parâmetros (valor, moeda,
item, origem). Relatório útil não vem pronto — vem de escolher quais eventos marcam conversão e
quais parâmetros permitem cortar o dado depois.

A consequência prática é desconfortável: **o relatório padrão quase nunca responde à sua
pergunta**. Ele mostra o que a ferramenta sabe medir sozinha, não o que o seu negócio decide.

## Exemplo
Duas empresas instalam a mesma ferramenta. A primeira define `iniciar_orcamento`,
`enviar_orcamento` e `orcamento_aprovado`, cada um com valor estimado. A segunda deixa o padrão.
Seis meses depois, a primeira sabe onde o funil vaza e quanto vale cada estágio; a segunda sabe
quantas pessoas visitaram o site.

## Aplicação
Comece pelo fim: escreva as três perguntas que você quer conseguir responder daqui a seis meses
e derive os eventos a partir delas. É o mesmo raciocínio do tópico de dashboard em [[mapa-marketing]] — instrumento serve
pergunta, não o contrário.

## Erros comuns
- Comparar número de ferramentas diferentes como se medissem a mesma coisa — janela de
  atribuição e definição de sessão diferem, e a divergência é esperada.
- Marcar como conversão qualquer microação; quando tudo é conversão, nada é.
- Confiar em amostragem sem saber que ela existe naquele relatório.

## Relacionado
[[rastreamento-de-eventos-e-pixel]] · [[medicao-do-lado-do-servidor]] · [[metricas-de-qualificacao-de-lead]]

## Conhecimento externo (fora das suas fontes)
> Não está em nenhuma fonte do `RAW/`. O mecanismo de evento e parâmetro é estável; nomes de
> relatório e limites de cada ferramenta mudam e devem ser conferidos na documentação vigente.
