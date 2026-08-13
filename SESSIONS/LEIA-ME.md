# SESSIONS — histórico das sessões

Uma nota por sessão: `AAAA-MM-DD-<disciplina>.md`. Duas sessões da mesma disciplina no mesmo
dia → sufixo `-2`.

**Não é transcript de chat.** É o registro do que mudou: veredito, diagnóstico do erro,
mudança de estado, próximo passo. O transcript literal está no histórico do chat e não tem
valor de memória.

## Papel no sistema — arquivo, não memória de trabalho

A IA **não lê** o histórico de sessões para retomar. Ela lê `INICIO.md` + `LEARNER/`.
Tudo que ainda importa de uma sessão já foi destilado para o LEARNER no momento em que
aconteceu.

Isso é deliberado: se retomar exigisse reler sessões, o custo cresceria para sempre e o
sistema quebraria no ano 2. Ver [[ARQUITETURA]], decisão sobre orçamento de leitura.

As sessões servem para:
- auditoria — "quando foi que eu errei isso pela primeira vez?"
- reconstruir o LEARNER se ele for corrompido ou apagado
- ver sua própria evolução ao longo dos meses

Se algo importante existe **só** numa sessão antiga e não no LEARNER, isso é um defeito:
peça um lint e destile para o LEARNER.
