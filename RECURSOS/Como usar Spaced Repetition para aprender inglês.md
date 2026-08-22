---
fontes:
---

# Como usar o Spaced Repetition pra aprender inglês neste vault

> Registrado em 2026-08-22, depois de decidir instalar o plugin **Spaced Repetition**
> (`obsidian-spaced-repetition`) — ver contexto em [[TAREFAS]] e exemplo pronto em
> [[exemplo-frases-coletadas]]. Resolve uma divisão de trabalho que já estava prevista em
> [[mapa-ingles]] (Fase 1, itens 4 e 5) mas sem ferramenta ainda.

## A divisão: LEARNER vs. plugin, sem redundância

Duas coisas diferentes, cada uma no lugar certo — nenhuma substitui a outra:

| | **LEARNER** (conversa comigo) | **Spaced Repetition** (plugin, dentro do Obsidian) |
|---|---|---|
| O que guarda | Gramática e método — present perfect, phrasal verbs, os próprios itens 4/5 da grade | Vocabulário e frase — potencialmente milhares de itens |
| Quantidade | Poucas dezenas (a grade de `ingles` tem 42 itens no total) | Cresce sem limite, um cartão por frase coletada |
| Avaliação | Conversacional — você explica, eu corrijo | Reconhecimento rápido — clica "lembrei" / "não lembrei" |
| Onde mora | `KNOWLEDGE/comunicacao/ingles/` + `LEARNER/estado-ingles.md` | `KNOWLEDGE/comunicacao/ingles/flashcards/` (tag `#flashcards`) |

## O princípio central (já estava na grade, item 5)
**O cartão nasce da frase que você coletou, não de lista de vocabulário pronta.** Lista temática
("cores em inglês", "animais em inglês") rende pouco porque a palavra fica sem contexto de uso
real — você lembra a palavra mas trava na hora de usar. Frase coletada já vem com colocação,
registro e contexto embutidos.

## O fluxo, passo a passo

1. **Encontre a frase.** Lendo, ouvindo, numa reunião, num vídeo — qualquer lugar onde você
   topar com uma palavra ou expressão nova, ou uma que reconhece mas ainda hesita.
2. **Capture a frase inteira**, não só a palavra. Mais rápido: seção "Captura rápida" do
   [[TAREFAS]] (ou o plugin QuickAdd, se configurar um atalho pra isso).
3. **Vire cartão** — formato simples de linha única:
   ```
   Frase em inglês — o que "expressão-alvo" significa?::Tradução/explicação + registro (formal/informal) + quando usar
   ```
   Ver [[exemplo-frases-coletadas]] pra mais formatos (reverso, multi-linha, cloze).
4. **Salve num arquivo com a tag `#flashcards`** no frontmatter — dentro de
   `KNOWLEDGE/comunicacao/ingles/flashcards/`. Pode ser um arquivo só crescendo, ou vários por
   tema/data — o plugin escaneia a tag, não importa quantos arquivos.
5. **Revise no Obsidian**, não comigo — paleta de comando → "Review flashcards" (ou o ícone na
   barra lateral). Isso roda fora da conversa, sem gastar tempo de sessão comigo.

## Quando pedir pra mim, em vez de fazer sozinho
- Transformar uma frase capturada em cartão formatado — cola a frase crua e eu devolvo no
  formato certo.
- Entender por que uma expressão significa o que significa (isso é ensino, fica em LEARNER se
  virar um padrão recorrente de erro/confusão).
- Revisar um lote de cartões pra ver se o registro (formal/informal) e a tradução estão certos.

## O que eu não vou fazer
Não vou tentar simular a revisão espaçada de vocabulário numa conversa comigo — isso é
exatamente o que o plugin já faz melhor, mais rápido, sem gastar token nem esperar resposta. Pedir
pra eu "testar seu vocabulário" vira uma sessão de LEARNER só se for sobre um padrão de erro
específico, não pra treinar volume de palavra.
