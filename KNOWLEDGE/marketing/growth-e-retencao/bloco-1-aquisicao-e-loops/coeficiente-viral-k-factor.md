---
tipo: conceito
disciplina: growth-e-retencao
titulo: Coeficiente viral: a conta que diz se o loop fecha
fontes: []
criado: 2026-08-20
atualizado: 2026-08-20
---

# Coeficiente viral: a conta que diz se o loop fecha

**Ideia central:** o coeficiente viral é o número de novos usuários que cada usuário existente
traz — e a régua é brutalmente simples: acima de 1, o crescimento se sustenta sozinho; abaixo,
cada onda é menor que a anterior.

## O mecanismo
```
k = convites por usuário x taxa de conversão do convite
```
Se cada usuário convida 10 pessoas e 8% aceitam, k = 0,8: cada 100 usuários geram 80, que geram
64, que geram 51. A série converge e para. Se k = 1,2, ela diverge.

**O segundo fator é o tempo de ciclo.** k = 1,1 com ciclo de um dia e k = 1,1 com ciclo de três
meses produzem realidades completamente diferentes. Crescimento viral é k **e** velocidade.

## Exemplo
Duas ferramentas com o mesmo k: numa, o convite acontece no primeiro uso; na outra, só depois de
o usuário montar um projeto inteiro. A primeira cresce em semanas, a segunda em anos — mesma
matemática, resultados incomparáveis.

## Aplicação
k abaixo de 1 não é fracasso: quase todo negócio real vive assim, e viralidade parcial **reduz
o custo de aquisição** em vez de eliminá-lo. Trate como desconto no custo, não como plano de
crescimento.

## Erros comuns
- Confundir compartilhamento com conversão — convite enviado não é usuário novo.
- Ignorar o tempo de ciclo.
- Contar como viral o crescimento que veio de verba paga no mesmo período.

## Relacionado
[[growth-hacking-e-loop-viral]] · [[onboarding-e-ativacao]] · [[analise-de-coorte]]

## Conhecimento externo (fora das suas fontes)
> Não está em nenhuma fonte do `RAW/`. Mecanismo estável, sem número de referência —
> os benchmarks que circulam nesta área vêm de amostras de empresas financiadas por
> capital de risco e não transferem para outro contexto.
