---
tipo: nota-pessoal
categoria: observacao
autor: tiago
criado: 2026-08-15
triada: sim
---

# O padrão LLM Wiki (Karpathy) — por que este vault existe

> Síntese de três capturas do INBOX (dois artigos clipados sobre o padrão, mais o documento
> original do Karpathy), não reprodução literal — os originais ficaram no INBOX se você
> quiser reler na íntegra.

## A ideia central

RAG tradicional (upload de arquivo, busca por trecho na hora da pergunta) não acumula nada —
a IA "redescobre" o conhecimento a cada pergunta. Andrej Karpathy propôs em abril de 2026 uma
alternativa: a IA mantém uma **wiki pessoal persistente e interligada** que cresce a cada
fonte nova — não só indexa, mas reescreve página de entidade, atualiza síntese, sinaliza
contradição com o que já existia. O conhecimento é compilado uma vez e **mantido atualizado**,
não recalculado do zero a cada pergunta.

Karpathy descreve a divisão de papéis assim: Obsidian é o armazenamento (texto puro, seu,
local); a IA é quem lê o cofre inteiro, arquiva, liga e responde. "Obsidian é a IDE; a IA é o
programador; a wiki é o código."

## Onde isso já é este vault

Não é teoria abstrata pra você — é o que já está rodando:

- `LEARNER/` é a wiki se atualizando (estado do aluno, reescrito a cada veredito, não
  redescoberto do zero)
- `KNOWLEDGE/` é a wiki do assunto, com contradição entre fontes sinalizada, não resolvida em
  silêncio (`CLAUDE.md` invariante 5)
- `SESSIONS/` é o arquivo morto — histórico que não precisa ser relido, porque o que importa
  já foi destilado pro LEARNER
- `index.md` é o MOC (mapa de conteúdo) que Karpathy descreve como porta de entrada

## Relacionado
[[ARQUITETURA]] — o desenho de fato deste vault, incluindo por que cada camada existe

## Fontes originais (preservadas no INBOX)
- Link da fonte original: [Yarchi no X](https://x.com/undefinedKi/status/2068306794116501544)
- [Crie um Segundo Cérebro com IA — Gustluiz, Substack](https://substack.com/home/post/p-206615827)
- Documento original do Karpathy: "LLM Wiki" (capturado como `llm-wiki - Copia.md`)
![[llm-wiki - Copia]]