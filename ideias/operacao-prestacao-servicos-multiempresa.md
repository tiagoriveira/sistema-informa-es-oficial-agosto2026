---
tipo: ideia
status: em_maturacao
criado: 2026-08-16
atualizado: 2026-08-16
---

# Operação de prestação de serviços para múltiplas empresas

**Ideia central:** manter o vault pessoal agnóstico e criar, quando a operação existir, uma
área de prestação de serviços com contexto isolado para cada empresa atendida.

*## Contexto da ideia

O vault foi criado primeiro para estudo e construção de conhecimento pessoal. Surgiu a hipótese
de usá-lo também para orquestrar uma atuação profissional de marketing e prestação de serviços.

A primeira alternativa seria refatorar a arquitetura inteira para ela passar a girar em torno da
empresa. Isso foi rejeitado: transformaria um sistema pessoal e geral em um sistema especializado
antes de haver operação real, e dificultaria usá-lo para outras áreas da vida e do aprendizado.

A alternativa escolhida é modular: o sistema principal continua agnóstico; a futura operação é
um braço dentro dele. Isso permite atender várias empresas sem misturar os seus contextos e sem
criar um vault separado para cada cliente.

## Princípio

O STUDY-BRAIN continua sendo o sistema pessoal central: estudo, vida e trabalho convivem no
mesmo vault. A operação de serviços não deve refatorar nem substituir a arquitetura geral.

Como prestação de serviços é uma responsabilidade contínua, seu lugar é `AREAS/`, não
`PROJETOS/`. Projetos são entregas delimitadas dentro dessa área.

O PARA dentro de cada cliente não substitui o PARA da raiz. Ele é apenas uma visão local: ajuda
a separar entregas, responsabilidades contínuas, referências e material encerrado daquele
cliente específico.

## Estrutura proposta

```text
AREAS/
└── prestacao-de-servicos/
    ├── operacao.md
    ├── clientes/
    │   └── <cliente>/
    │       ├── contexto-cliente.md
    │       ├── PROJETOS/
    │       ├── AREAS/
    │       ├── RECURSOS/
    │       └── ARQUIVADOS/
    └── processos/
```

`operacao.md` concentra a oferta, o posicionamento, os critérios de cliente, o processo e os
ativos reutilizáveis. Cada `contexto-cliente.md` concentra negócio, público, oferta, tom de
voz, histórico, restrições e decisões daquele cliente.

## Problema que resolve

Sem essa fronteira, uma estratégia, objeção, dado ou tom de voz de um cliente pode contaminar a
decisão tomada para outro. A IA passaria a responder com contexto genérico ou, pior, com o
contexto errado. O objetivo da estrutura é permitir que cada trabalho seja retomado com poucas
leituras: operação → cliente → projeto ativo.

## Regras de operação propostas

- Ao trabalhar para um cliente, ler apenas o contexto da operação, do cliente e do projeto
  ativo; não assumir dados de outros clientes.
- Material reutilizável de marketing permanece em `KNOWLEDGE/marketing/`; material específico
  fica no cliente.
- Usar nomes únicos no vault: `briefing-acme.md`, não `briefing.md`.
- Campanha, lançamento ou entrega com prazo vira projeto dentro do cliente; relação contínua
  vira área dentro do cliente.
- Encerrado o cliente ou a iniciativa, mover o material para o `ARQUIVADOS/` daquele cliente.

## Decisão

Em aberto. Criar a área somente quando houver uma operação de prestação de serviços real ou o
primeiro cliente; antes disso, esta nota é referência de desenho, não estrutura a manter.

**Gatilho de implementação:** primeiro serviço em andamento ou necessidade concreta de manter
contexto recorrente de um cliente. Até esse momento, não criar pastas vazias, processos ou
painéis só para “deixar pronto”.


> # **É UMA MERA IDEIA EM MATURAÇÃO E NÃO DEVE SER CONSIDERADA COMO FATO OU DOGMA A SER SEGUIDO**
