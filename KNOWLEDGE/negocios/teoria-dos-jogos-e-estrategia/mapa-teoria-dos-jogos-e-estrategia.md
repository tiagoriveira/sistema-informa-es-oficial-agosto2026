---
tipo: mapa
disciplina: teoria-dos-jogos-e-estrategia
hub: negocios
atualizado: 2026-08-16
---

# Mapa — Teoria dos Jogos e Estratégia

**Fontes desta disciplina:** nenhuma em `RAW/` — grade checada por busca na web em 2026-08-16
(ver "Nota sobre a grade"), não só memória de treino.
**Estado do aluno:** [[estado-teoria-dos-jogos-e-estrategia]]

**Fronteira com [[mapa-frameworks-de-pensamento]]:** lá o ambiente é fixo e você decide sozinho
contra a incerteza; aqui o resultado depende da jogada de outro agente racional que também está
tentando prever você. É decisão em segunda ordem: "o que ele vai fazer, sabendo o que eu sei que
ele sabe" — não cabe na Fase 3 de frameworks, que é sobre probabilidade, não sobre outro jogador.

**Fronteira com [[mapa-poder-e-dinamica-social]]:** lá é como poder e persuasão funcionam entre
pessoas em geral; aqui é o cálculo formal por trás de uma classe específica de interação —
quando cooperar, quando trair, quando blefar — com payoff explícito.

## Ordem de estudo sugerida
_(status derivado do LEARNER — não editar à mão, regenerado a cada UPDATE. `CLAUDE.md` §4.2:
esta ordem não é dogma, desvie quando houver motivo)_

### Fase 1 — A estrutura de um jogo
1. 📍 O que faz algo ser um "jogo": jogadores, estratégias, payoff e informação
2. ⬜ Jogos simultâneos vs. sequenciais — decidir junto ou decidir sabendo o que o outro já fez
3. ⬜ Forma normal (matriz) vs. forma extensiva (árvore) — duas formas de desenhar o mesmo jogo
4. ⬜ Informação completa vs. incompleta — o que cada jogador sabe sobre o outro

### Fase 2 — Equilíbrio: prever a jogada racional do outro
5. ⬜ Estratégia dominante e eliminação iterada de estratégias dominadas
6. ⬜ Equilíbrio de Nash: ninguém melhora mudando sozinho de estratégia
7. ⬜ Dilema do Prisioneiro: por que dois racionais chegam ao pior resultado conjunto
8. ⬜ Jogo de coordenação e Batalha dos Sexos — quando o problema é só combinar, não competir
9. ⬜ Estratégia mista e equilíbrio em jogos sem solução pura (par-ou-ímpar, pênalti)
10. ⬜ Subgame perfection e indução retroativa — resolver a árvore de trás pra frente

### Fase 3 — Quando o jogo se repete ou a informação é assimétrica
11. ⬜ Jogos repetidos: por que cooperação pode emergir sem contrato (tit-for-tat, sombra do futuro)
12. ⬜ Jogo do Confiança e do Caça ao Cervo (Stag Hunt) — cooperação como equilíbrio frágil
13. ⬜ Sinalização (signaling): gastar recurso só para provar um tipo que o outro não vê
14. ⬜ Triagem (screening) e seleção adversa — desenhar a oferta pra separar tipos de jogador
15. ⬜ Risco moral (moral hazard) — o incentivo muda depois que o contrato já foi assinado
16. ⬜ Compromisso crível e o valor de queimar a própria opção de recuar

### Fase 4 — Aplicação em negociação e mercado
17. ⬜ Barganha sequencial e o custo da impaciência — quem cede primeiro perde valor
18. ⬜ BATNA e ponto de reserva — o preço de não fechar acordo nenhum
19. ⬜ Leilões: primeiro preço, segundo preço (Vickrey), inglês e holandês — quando cada um serve
20. ⬜ Coalizão e poder de barganha em jogos de N jogadores
21. ⬜ Jogo do Ultimato e do Ditador — onde a racionalidade pura prevê errado o comportamento real
22. ⬜ Aplicação em precificação, guerra de lances e entrada em mercado competitivo

## Nota sobre a grade
Grade desenhada em 2026-08-16 a partir de busca na web (regra `CLAUDE.md` §6): Fase 1 monta o
vocabulário (o que é um jogo), Fase 2 resolve o jogo estático clássico (equilíbrio), Fase 3
entra na complicação real — repetição e informação incompleta, onde a maior parte do valor
prático mora — e Fase 4 aplica tudo em negociação e mercado, o destino mais comum do assunto
fora da sala de aula.

Núcleo (Fases 1-2) é **estável desde os anos 1950** (von Neumann, Nash) e não envelhece. Fase 4
é onde a aplicação prática em negócio se atualiza mais rápido (design de leilão, mercados
digitais).

**Fontes consultadas:**
- [Game Theory — Open Yale Courses](https://oyc.yale.edu/economics/econ-159)
- [Welcome to Game Theory — Coursera/University of Tokyo](https://www.coursera.org/learn/game-theory-introduction)
- [Game Theory — Stanford/Coursera](https://www.coursera.org/learn/game-theory-1)
- [Rutgers Business School — Game Theory PhD Syllabus](https://www.business.rutgers.edu/sites/default/files/documents/phd-syllabus-game-theory.pdf)
- [A Definitive Guide to Negotiation and Game Theory](https://www.numberanalytics.com/blog/definitive-guide-negotiation-game-theory)
- [The Ultimate Guide to Bargaining in Game Theory](https://www.numberanalytics.com/blog/ultimate-bargaining-problem-guide)
