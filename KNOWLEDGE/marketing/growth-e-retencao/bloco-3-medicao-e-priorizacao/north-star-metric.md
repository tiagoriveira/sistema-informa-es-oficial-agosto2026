---
tipo: conceito
disciplina: growth-e-retencao
titulo: North star metric: a métrica única, e por que ela costuma ser mal escolhida
fontes: []
criado: 2026-08-20
atualizado: 2026-08-20
---

# North star metric: a métrica única, e por que ela costuma ser mal escolhida

**Ideia central:** é a métrica que melhor representa **o valor entregue ao cliente** e que, se
subir, puxa a receita junto — e o teste que a valida é o inverso: se ela subir e a receita não
vier, você escolheu errado.

## O mecanismo
Uma boa métrica-guia tem três propriedades:
1. **Reflete valor recebido**, não esforço da empresa. Número de anúncios publicados é esforço;
   número de entregas concluídas é valor.
2. **É acionável pelos times** — dá para influenciar por produto, marketing e suporte.
3. **Antecede a receita**, servindo de indicador antecedente e não de espelho atrasado.

O erro estrutural é escolher uma métrica de volume que pode subir enquanto o cliente piora.
Isso é a Lei de Goodhart chegando pela porta da frente: assim que a métrica vira alvo, ela
deixa de medir o que media.

## Exemplo
Uma plataforma escolhe "usuários ativos por mês". O time otimiza notificação, o número sobe,
o cancelamento sobe junto. Trocar para "usuários que concluíram a ação de valor na semana"
muda o comportamento do time inteiro — sem mudar nenhuma meta de receita.

## Aplicação
Escolha uma, com no máximo três métricas de apoio que capturem o efeito colateral que a
principal pode causar. E revise quando o negócio mudar de estágio: a métrica certa na
validação não é a certa na escala.

## Erros comuns
- Escolher receita como métrica-guia — é resultado, não guia.
- Ter cinco "métricas principais", o que é o mesmo que não ter nenhuma.
- Não medir o dano colateral do alvo escolhido.

## Relacionado
[[okr-de-marketing]] · [[analise-de-coorte]] · [[mapa-fundamentos-sistemas-gestao]]

## Conhecimento externo (fora das suas fontes)
> Não está em nenhuma fonte do `RAW/`. Mecanismo estável, sem número de referência —
> os benchmarks que circulam nesta área vêm de amostras de empresas financiadas por
> capital de risco e não transferem para outro contexto.
