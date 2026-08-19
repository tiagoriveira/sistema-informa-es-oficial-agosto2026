---
tipo: mapa
disciplina: arquitetura-de-agentes-e-contexto
hub: inteligencia-artificial
atualizado: 2026-08-19
---

# Mapa — Arquitetura de Agentes e Contexto

**Fontes desta disciplina:** nenhuma em `RAW/` — grade checada por busca na web em 2026-08-19
(ver "Nota sobre a grade"), não só memória de treino.
**Estado do aluno:** [[estado-arquitetura-de-agentes-e-contexto]]

**Origem:** pedido do Tiago em 2026-08-19, a partir do curso "Ratos OS" (Claude Code como
sistema operacional de negócio) e de uma resposta do Grok que sugeria criar disciplina nova.
Checado contra o vault antes de criar — o tema já aparecia distribuído (superficialmente) em
três disciplinas; esta existe pra aprofundar a camada **aplicada e agnóstica de domínio**, sem
duplicar as outras.

**Fronteiras** (evita sobreposição):
- **[[mapa-colaboracao-humano-ia]]** (mesmo hub) fica com a camada humana/decisão — quando
  automatizar, onde colocar aprovação, como verificar saída. Aqui é a **camada de arquitetura**:
  como o arquivo/pasta/skill precisa estar montado pra aquilo funcionar.
- **[[mapa-dados-estatistica-e-ia-ml]]** (hub tecnologia) fica com o funcionamento interno do
  modelo (estatística, treino, como um LLM gera texto). Aqui não interessa como o modelo
  funciona por dentro, só como estruturar o que ele lê e como ele age no mundo.
- **[[mapa-gestao-conhecimento-second-brain]]** (hub gestao-sistemas) fica com o método de PKM
  em si (CODE, PARA, Zettelkasten), que vale com ou sem IA. Aqui o second brain é só **um
  exemplo de sistema** entre outros (o outro exemplo típico é negócio/produto, caso do curso
  Ratos OS) — o foco é o padrão de arquitetura, não o método de anotar.

## Ordem de estudo sugerida
_(status derivado do LEARNER — não editar à mão, regenerado a cada UPDATE. `CLAUDE.md` §4.2:
esta ordem não é dogma, desvie quando houver motivo)_

### Fase 1 — Arquivos de contexto persistente
1. ⬜ Hierarquia de arquivos de instrução (CLAUDE.md / AGENTS.md / SKILLS.md / CONTEXT.md) —
   qual manda em cima de qual
2. ⬜ Escopo e herança — regra global do sistema vs. regra por pasta/projeto/cliente
3. ⬜ O que vai em instrução persistente vs. o que vai em prompt pontual da conversa
4. ⬜ Memória de longo prazo: arquivo plano, banco estruturado ou busca semântica — trade-off
   de cada abordagem

### Fase 2 — Skills e componentes reutilizáveis
5. ⬜ Skill como unidade de capacidade configurada uma vez, reusada muitas
6. ⬜ Quando extrair uma skill vs. deixar solto no prompt — o critério de reuso
7. ⬜ Composição: tarefa complexa como cadeia de skills menores, não um prompt gigante
8. ⬜ Versionamento e manutenção de skill — ela envelhece, quebra e precisa de dono

### Fase 3 — Arquitetura de pasta como base de conhecimento
9. ⬜ Pasta como unidade de contexto — "cada pasta é a entidade real" (empresa, projeto,
   cliente, disciplina)
10. ⬜ Pipeline de ingestão: fonte bruta → processada → indexada (equivalente ao próprio
    RAW → KNOWLEDGE deste vault)
11. ⬜ Convenção de nome e estrutura — a IA não adivinha organização, ela lê convenção
12. ⬜ Lint/auditoria como manutenção contínua — órfã, duplicata, contradição, conteúdo
    desatualizado

### Fase 4 — Orquestração multi-agente
13. ⬜ Padrões de orquestração: pipeline, fan-out, supervisor, debate, swarm — quando usar
    cada um
14. ⬜ Padrão supervisor — por que virou o default de 2026 na maioria dos frameworks
15. ⬜ Protocolo agente-agente (A2A) e orquestração descentralizada — estado emergente, ainda
    imaturo
16. ⬜ Simplicidade primeiro — sofisticação de orquestração deve seguir a complexidade da
    tarefa, não precedê-la

### Fase 5 — Confiabilidade e operação
17. ⬜ Testar o fluxo completo, não só o agente isolado — falha emerge da interação entre
    agentes, não só de um agente sozinho
18. ⬜ Fallback e tratamento de erro entre agentes
19. ⬜ Onde colocar o ponto de aprovação humana na arquitetura (conecta com
    [[operador-centauro]])
20. ⬜ Custo e latência como restrição de design desde o início, não detalhe de implementação
    posterior

## Nota sobre a grade
Grade desenhada em 2026-08-19 a partir de busca na web (regra `CLAUDE.md` §6). Área muito nova
e que muda rápido — em 2026 a indústria está convergindo pra uma arquitetura com camadas
(arquivo de contexto no nível de projeto → skills portáteis → MCP pra acesso a ferramenta →
recuperação dinâmica pro resto), e pra orquestração multi-agente o padrão "supervisor" é hoje o
default mais usado, com protocolos agente-a-agente (A2A) ainda emergentes. Recheck obrigatório
antes de estudar Fases 3-5.

**Fontes consultadas:**
- [Effective context engineering for AI agents — Anthropic](https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents)
- [Claude.md vs Agents.md vs Memory.md, Skills.md, Context.md & The Hierarchy (2026 Guide) — Amit Ray](https://amitray.com/claude-md-vs-agents-md-memory-md-skills-md-context-md-guide-2026/)
- [Context Engineering for AI Agents | SKILL.md Guide — Agensi](https://www.agensi.io/learn/context-engineering-ai-agents)
- [Multi-Agent Orchestration: 5 Patterns That Work in 2026 — Digital Applied](https://www.digitalapplied.com/blog/multi-agent-orchestration-5-patterns-that-work)
- [6 Multi-Agent Orchestration Patterns for Production (2026) — Beam AI](https://beam.ai/agentic-insights/multi-agent-orchestration-patterns-production)
- [AI Agent Orchestration Best Practices: Production Guide 2026 — AI Agents Plus](https://www.ai-agentsplus.com/blog/ai-agent-orchestration-best-practices-march-2026)
