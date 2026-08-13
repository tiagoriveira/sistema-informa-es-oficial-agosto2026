# LEARNER — modelo do aluno

O que **você** sabe, não sabe e confunde. É a memória que faz a IA retomar de onde parou.
Escrito pela IA automaticamente, durante a sessão (não só no fim).

```
LEARNER/
├── perfil.md              ← vale para todas as disciplinas
├── estado-economia.md     ← um arquivo por disciplina
└── estado-filosofia.md
```

**Um arquivo por disciplina, um bloco por conceito.** Todas as dimensões do mesmo conceito
(estado, evidências, confusões, próximo passo, agendamento) ficam juntas no mesmo bloco.
Atualizar um conceito é editar um lugar só.

## Vocabulário fechado (não é nota, é classificação com critério)

| Estado | Critério |
|---|---|
| `nao_iniciado` | nunca avaliado, ou só lido |
| `fragil` | na última avaliação não explicou, ou explicou errado |
| `em_desenvolvimento` | já explicou certo, mas com hesitação, ajuda, ou errou em outra ocasião |
| `consolidado` | explicou certo e sem ajuda em 2+ ocasiões em dias diferentes, incluindo uma recuperação após 7+ dias |

Não existe porcentagem, nota nem barra de progresso — por decisão de projeto. Ver
[[ARQUITETURA]], decisão sobre métricas.

## Revisão espaçada

`nivel` é contador de agendamento, não medida de conhecimento.
1→1 dia · 2→3 dias · 3→7 dias · 4→16 dias · 5→35 dias

acertou sem ajuda → sobe 1 · com hesitação → mantém · errou → cai para 1 ·
confundiu com outro conceito → cai para 1 e os dois entram em revisão comparativa.

O que está agendado:

```bash
grep -rn "revisar:" LEARNER/
```

## Você pode editar

Se um registro estiver errado ("marquei como frágil algo que você domina"), diga na conversa —
a IA corrige e registra a correção. Editar à mão também funciona, mas avise na sessão seguinte
para não haver divergência entre o arquivo e o que a IA acha que sabe.
