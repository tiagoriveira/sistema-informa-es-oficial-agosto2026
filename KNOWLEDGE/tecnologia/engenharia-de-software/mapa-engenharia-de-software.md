---
tipo: mapa
disciplina: engenharia-de-software
hub: tecnologia
atualizado: 2026-08-17
---

# Mapa — Engenharia de Software

**Fontes desta disciplina:** nenhuma em `RAW/` — grade checada por busca na web em 2026-08-17
(ver "Nota sobre a grade").
**Estado do aluno:** [[estado-engenharia-de-software]]

**Pré-requisito:** [[mapa-fundamentos-de-programacao]] — aqui já se assume lógica, estrutura de
dado e OOP resolvidos. **Fronteira com [[mapa-tecnologia-para-fundadores]]:** aqui é como
construir; lá é como decidir e gerenciar sem construir.

## Ordem de estudo sugerida
_(status derivado do LEARNER — não editar à mão, regenerado a cada UPDATE. `CLAUDE.md` §4.2:
esta ordem não é dogma, desvie quando houver motivo)_

### Fase 1 — Arquitetura e organização de código
1. ⬜ Padrões de design — problemas recorrentes, soluções com nome
2. ⬜ Princípios SOLID e código limpo
3. ⬜ Arquitetura MVC — separar dado, lógica e apresentação
4. ⬜ Controle de versão em equipe — branch, merge, code review

### Fase 2 — Dados e persistência
5. ⬜ Bancos relacionais (SQL) — modelagem e consulta
6. ⬜ Bancos não-relacionais (NoSQL) — quando faz sentido
7. ⬜ Migração e versionamento de schema
8. ⬜ Cache — por que e onde acelerar leitura

### Fase 3 — APIs e comunicação entre sistemas
9. ⬜ REST API — design de endpoint, verbo HTTP, status code
10. ⬜ Autenticação e autorização — quem é e o que pode fazer
11. ⬜ Como a rede funciona — cliente-servidor, DNS, HTTP/HTTPS
12. ⬜ Mensageria e fila — comunicação assíncrona entre serviços

### Fase 4 — Qualidade e confiabilidade
13. ⬜ Testes automatizados — unitário, integração, e2e
14. ⬜ Debugging e observabilidade — log, métrica, tracing
15. ⬜ CI/CD — integração e entrega contínua
16. ⬜ Segurança básica de aplicação — OWASP top 10

### Fase 5 — Design de sistemas em escala
17. ⬜ Escalabilidade — vertical vs. horizontal
18. ⬜ Load balancing e CDN
19. ⬜ Microsserviços vs. monolito — o trade-off real
20. ⬜ Consistência e tolerância a falha em sistema distribuído

## Nota sobre a grade
Grade desenhada em 2026-08-17 a partir de busca na web (regra `CLAUDE.md` §6). Ordem:
organização de código → dado → comunicação entre sistemas → qualidade → escala, que é a
progressão que roadmaps atuais de engenharia de software usam pra ir de "sabe programar" a
"sabe construir sistema". Fase 5 (design de sistema distribuído) é a que mais acelera com IA
mudando prática de observabilidade e teste — recheck mais frequente que as demais.

**Fontes consultadas:**
- [Software Engineering Syllabus 2026 — Scaler](https://www.scaler.com/blog/software-engineering-syllabus/)
- [System Design Roadmap 2026 — Scaler](https://www.scaler.com/blog/system-design-roadmap-2026-complete-guide-from-beginner-to-advanced/)
- [Complete System Design Roadmap 2026 — Dev Kant Kumar](https://www.devkantkumar.com/blog/complete-system-design-roadmap-2026/)
