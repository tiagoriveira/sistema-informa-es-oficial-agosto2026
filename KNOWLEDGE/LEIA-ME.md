# KNOWLEDGE — conhecimento estruturado

Conhecimento **sobre o assunto**, não sobre você. O que você sabe ou não sabe fica em
`LEARNER/`. Essa separação é deliberada: as páginas daqui são estáveis e reutilizáveis;
seu estado é volátil e muda toda sessão.

Escrito pela IA, com sua aprovação para páginas novas. Você lê e corrige; não precisa escrever.

## Organização

```
KNOWLEDGE/
└── economia/
    ├── mapa-economia.md          ← MOC: ordem de estudo, o que existe, o que falta
    ├── oferta-e-demanda.md       ← conceitos, direto na raiz da disciplina
    ├── elasticidade-preco.md
    └── fontes/
        └── mankiw-cap-5.md       ← uma página por unidade ingerida
```

Conceitos ficam **planos** dentro da disciplina — sem subpastas por tema. Tema é seção no
`mapa-<disciplina>.md`, não pasta. Motivo: decidir em que pasta um conceito mora custa tempo
e não devolve nada; o mapa e os links fazem o trabalho melhor.

## Regras que valem sempre

- Nome de arquivo único no vault inteiro (`[[link]]` resolve por nome, não por caminho).
- Toda página cita a fonte: `(cf. [[fonte]], p. 42)`.
- Conhecimento que não veio das suas fontes vai em seção rotulada `## Conhecimento externo`.
- Fontes divergentes → `## Divergências entre fontes`, sem escolher um lado.
- Página nova só com sua aprovação. Na dúvida, não criar.

Formato completo em [[schema]].
