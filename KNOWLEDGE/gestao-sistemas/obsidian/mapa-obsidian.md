---
tipo: mapa
disciplina: obsidian
hub: gestao-sistemas
atualizado: 2026-08-15
---

# Mapa — Obsidian

**Fontes desta disciplina:** nenhuma em `RAW/` — grade checada por busca na web em 2026-08-15
(ver "Nota sobre a grade"), não só memória de treino.
**Estado do aluno:** [[estado-obsidian]]

**Fronteira com [[mapa-gestao-conhecimento-second-brain]]:** aqui é a **ferramenta** (como o
Obsidian funciona e o que ele te obriga a decidir); lá é o **método** (PARA, CODE,
Zettelkasten, sumarização progressiva). Método sem ferramenta é teoria; ferramenta sem método
é pasta bagunçada com grafo bonito.

## Ordem de estudo sugerida
_(status derivado do LEARNER — não editar à mão, regenerado a cada UPDATE. `CLAUDE.md` §4.2:
esta ordem não é dogma, desvie quando houver motivo)_

### Fase 1 — O modelo mental (por que não é "mais um app de notas")
1. 📍 O vault é uma pasta: markdown local, sem banco de dados, sem lock-in
2. ⬜ Local-first: o que você ganha (posse, longevidade) e o que passa a ser seu problema (backup, sync)
3. ⬜ Anatomia do vault: `.obsidian/`, config, workspace — o que versionar e o que ignorar
4. ⬜ Markdown do Obsidian: o padrão CommonMark e as extensões próprias (callouts, embeds, `%%comentários%%`)
5. ⬜ O que o Obsidian **não** faz: não organiza, não resume, não decide por você
6. ⬜ [[comandos-e-hotkeys-obsidian]] — a paleta como porta única; tecla dedicada só pro diário

### Fase 2 — Linkar em vez de arquivar
7. ⬜ `[[wikilink]]`: por que o Obsidian resolve link por nome de arquivo, e o que isso impõe
8. ⬜ Link para nota que não existe: criar clicando, deixar o vault crescer por demanda
9. ⬜ Backlinks e menções não linkadas — o painel que transforma nota em nó
10. ⬜ Embed e transclusão `![[nota#seção]]`: nota como bloco reutilizável
11. ⬜ Aliases, renomear com segurança e colisão de nomes entre disciplinas
12. ⬜ Grafo: o que ele mostra de útil, e por que é péssimo como métrica de progresso

### Fase 3 — Estrutura: metadados, tags e pastas
13. ⬜ Properties (frontmatter YAML): tipos, quando valem, quando viram dívida de manutenção
14. ⬜ Tag vs. pasta vs. link — três eixos diferentes, três usos que não se substituem
15. ⬜ MOC / hub note: índice escrito à mão como porta de entrada
16. ⬜ Templates e Templater: capturar sem redecidir o formato toda vez
17. ⬜ Daily notes e captura de baixa fricção — o inbox que evita a decisão prematura

### Fase 4 — Consultar o vault: de arquivo morto a base viva
18. ⬜ Busca: operadores (`file:`, `path:`, `tag:`, `line:`), aspas e regex
19. ⬜ **Bases** (core plugin, 2026): notas viram base de dados — views, filtros, fórmulas
20. ⬜ Dataview: o que ainda resolve, e por que hoje Bases vem primeiro
21. ⬜ Canvas: pensar no espaço; canvas como painel de comando sobre notas existentes
22. ⬜ O risco da automação: vault que só a query entende e ninguém mais lê

### Fase 5 — Sistema durável
23. ⬜ Plugins: core vs. comunidade — critério de adoção e risco de dependência
24. ⬜ Sync, Publish e alternativas (Git, iCloud, Syncthing): trade-offs reais
25. ⬜ Git como backup e histórico — versionar conhecimento, não só código
26. ⬜ Manutenção: links quebrados, notas órfãs, duplicatas, quando podar
27. ⬜ Obsidian + IA: o vault como contexto de longo prazo, e onde terceirizar destrói o aprendizado

## Nota sobre a grade

Grade desenhada em 2026-08-15 a partir de busca na web (regra `CLAUDE.md` §6), porque o
Obsidian mudou de forma relevante entre 2025 e 2026 e ensinar de memória arriscaria conteúdo
obsoleto. Duas mudanças que a grade já incorpora:

- **Bases virou core plugin** (2026) e ocupa o lugar que Dataview tinha como caminho padrão
  para dashboards — por isso o tópico 18 vem antes do 19, e o 19 é sobre *quando ainda vale*
  Dataview, não sobre aprendê-lo primeiro.
- **O app é gratuito inclusive para uso comercial**; o que se paga são serviços opcionais
  (Sync, Publish) e a licença comercial voluntária. Isso muda a conversa do tópico 24: a
  decisão é técnica (o que você quer que atravesse dispositivos), não de licença.

Tópico 6 (command palette e hotkeys) acrescentado em 2026-08-15 a pedido do Tiago,
renumerando os seguintes. A fase 1 falava do modelo mental e pulava direto para links, sem
passar por *como se opera* a ferramenta.

Lógica da ordem: fases 1-2 são o que não dá para pular — quem entende que "o vault é uma
pasta" e que "o link é o gesto principal" já usa o Obsidian direito, mesmo sem plugin nenhum.
A fase 3 é onde a maioria erra por excesso (metadado que ninguém consulta). A fase 4 só faz
sentido depois que existe massa de notas para consultar. A fase 5 é o que decide se o vault
sobrevive ao ano 2.

O que envelhece mais rápido: fases 4 e 5 (Bases é recente e ainda muda; o ecossistema de
plugins gira todo mês). Fases 1-3 são estáveis há anos.

**Meta-observação:** este vault é um caso de estudo da disciplina. `[[schema]]` §0 documenta a
decisão de resolver link por nome de arquivo (tópico 6); [[index]] é um MOC (tópico 14); o
LINT do `CLAUDE.md` §4 é o tópico 25 já implementado.

**Fontes consultadas:**
- [Obsidian Roadmap — obsidian.md](https://obsidian.md/roadmap/)
- [Obsidian Bases — When Your Notes Become a Database](https://minssam.com/en/blog/obsidian-bases-plugin-2026/)
- [The Ultimate Beginner's Guide to Obsidian — Sébastien Dubois (jul/2026)](https://www.dsebastien.net/the-ultimate-beginners-guide-to-obsidian/)
- [The Complete Guide to Dataview in Obsidian — Sébastien Dubois (ago/2026)](https://www.dsebastien.net/the-complete-guide-to-dataview-in-obsidian/)
- [Obsidian Canvas: A Complete Guide — Obsibrain](https://www.obsibrain.com/blog/obsidian-canvas-complete-guide)
- [Obsidian Properties: The Complete Guide — Obsidian Mate](https://obsidianmate.com/article/obsidian-properties-complete-guide)
- [Obsidian is Now Free for Commercial Use — Smartt](https://www.smartt.com/insights/obsidian-is-now-free-for-commercial-use-why-it-matters-for-your-business-and-security)
- [Obsidian Pricing 2026: Should You Pay for Sync or Publish?](https://aiproductivity.ai/blog/obsidian-pricing/)
- [Command palette — Obsidian Help](https://obsidian.md/help/plugins/command-palette) (tópico 6)
- [Editing shortcuts — Obsidian Help](https://obsidian.md/help/Editing+and+formatting/Editing+shortcuts) (tópico 6)
- [Hotkeys — Obsidian Help](https://obsidian.md/help/hotkeys) (tópico 6)
