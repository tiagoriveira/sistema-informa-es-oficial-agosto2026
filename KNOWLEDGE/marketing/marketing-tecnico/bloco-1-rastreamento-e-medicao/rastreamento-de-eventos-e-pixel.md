---
tipo: conceito
disciplina: marketing-tecnico
titulo: Rastreamento de eventos: tag manager, pixel e a camada de dados
fontes: []
criado: 2026-08-20
atualizado: 2026-08-20
---

# Rastreamento de eventos: tag manager, pixel e a camada de dados

**Ideia central:** o pixel não "vê" o que o usuário faz — ele só recebe os eventos que alguém
decidiu disparar, com os parâmetros que alguém decidiu mandar; rastreamento é uma decisão de
projeto, não uma consequência automática de instalar um código.

## O mecanismo, em três camadas
1. **Camada de dados.** O site publica um objeto com o que aconteceu — nome do evento, valor,
   identificador do produto, estágio do funil. É a fonte da verdade.
2. **Gerenciador de tags.** Lê a camada de dados e decide **quais** plataformas recebem
   **quais** eventos, com que parâmetro e sob que condição (inclusive consentimento).
3. **Destino.** Cada plataforma recebe o evento no formato dela — analytics, plataforma de
   anúncio, CRM.

Sem a camada 1, cada tag lê o HTML por conta própria e quebra na primeira mudança de layout.

## Exemplo
Um formulário de orçamento gera o evento `gerar_lead` com `valor_estimado` e `origem`. O
gerenciador manda para o analytics sempre, para a plataforma de anúncio só se houver
consentimento de marketing, e para o CRM com o identificador do lead. Um evento, três destinos,
uma decisão explícita em cada.

## Aplicação
Antes de instalar qualquer coisa: escreva a lista de eventos que o negócio precisa medir e o
que cada um carrega. **Plano de medição vem antes de tag.** Instalar primeiro e decidir depois
produz seis meses de dado que não responde à pergunta que interessa.

## Erros comuns
- Disparar evento no clique do botão em vez de na confirmação — infla conversão com tentativa.
- Nomear evento de forma inconsistente entre páginas, o que impede agregação depois.
- Medir tudo "porque é de graça": volume de evento sem pergunta associada vira ruído.
- Esquecer que o evento do navegador é bloqueável — ver [[medicao-do-lado-do-servidor]].

## Relacionado
[[medicao-do-lado-do-servidor]] · [[analytics-de-evento]] · [[auditoria-tecnica-de-conversao]]

## Conhecimento externo (fora das suas fontes)
> Não está em nenhuma fonte do `RAW/`. Mecanismo estável; a implementação concreta muda por
> plataforma e deve ser conferida na documentação vigente antes de configurar.
