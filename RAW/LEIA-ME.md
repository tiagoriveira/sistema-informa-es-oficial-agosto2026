# RAW — fontes originais

**Só o Tiago escreve aqui. A IA nunca edita, move, renomeia nem "organiza" nada nesta pasta.**

Esta é a camada de verdade. Tudo em `KNOWLEDGE/` é derivado daqui e pode ser reconstruído;
o que está aqui, não.

## Organização

Uma pasta por disciplina, com o nome em kebab-case:

```
RAW/
├── economia/
│   ├── mankiw-introducao-economia.pdf
│   └── artigo-elasticidade-fgv.md
└── filosofia/
    └── warburton-breve-historia-filosofia.pdf
```

Sem subpastas por tipo de mídia (livros/artigos/vídeos). O tipo é metadado da página de fonte,
não pasta — você sempre busca por assunto, nunca por "quero um PDF qualquer".

Fonte que serve a duas disciplinas: guarde na principal e cite a outra na página de fonte.

## Nomes de arquivo

`autor-titulo-curto.ext`. Sem acento, sem espaço, minúsculas.

## Formatos que funcionam

| Formato | Observação |
|---|---|
| `.md`, `.txt` | ideal |
| `.pdf` | funciona; PDF escaneado sem OCR não |
| `.epub` | converta para `.md` antes |
| vídeo / áudio | salve a transcrição como `.md` |
| página web | Obsidian Web Clipper → `.md` |

## Livro grande

Não peça para ingerir 400 páginas de uma vez — o resumo sai raso. Ingira **um capítulo por
vez**: uma página de fonte por capítulo, mais uma página-mãe do livro.
