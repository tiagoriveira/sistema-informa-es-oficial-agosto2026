# [[Ideia de criar post linkedin a partir de alguma de nossa base de informação]]

[[mapa-estatistica-para-decisao-marketing]]


# Trazer cursos transcritos
ver posts no reddit sobre obsidian e second brain
ver video elon musk sobre simplificar
- [ ] ler capitulo 6 continuar segundo cérebro
- [ ] trazer materias escrita, oratoria, hub de sedução, materias founder, product manager- materias do elon musk ( complementar abranger )

exemplo skiils aplicado a nosso projeto

> [!teste] Ideia de serviço
> Conteúdo
Ideia de projeto de auxilio com processos + marketing - vamos utilizar como braço de nossa prestação de serviço a stack do obsidian + claude como ferramentas - precisamos resolver um problema latente deles, ter sempre dados, oferecer melhorias e clareza! inclusive talvez de pra reaproveitar algo dessas duas notas do meu notion para arquitetar o serviço: [(2) NOTA IA CLAUDE COMO FOUNDER SOLO EM 2026 | Notion](https://app.notion.com/p/NOTA-IA-CLAUDE-COMO-FOUNDER-SOLO-EM-2026-37fa16ed6e5f80b38d51f783d8ace0cb?p=37da16ed6e5f8062a481d5c64d0698e9&pm=s) - essa notaesta em meu notion! essas notas são antigas e muita coisa ja mudou então não precisa seguir como dogmas! o job da solução talvez possa ser - minha ideia é começar a criar conteúdo no instagram [[mapa-producao-de-conteudo]] carrosel, fazer um mvp de conteúdos, ve como será o e ngajamento e aos poucos ir depois expandindo a produção de cnteúdos!


- [ ] Ver curso growth marketing com Fernando Miranda

ikigai vem como um dos principios para guiar nossas decisões - ex: essa minha iniciativa se alinha com o meu ikigai ? 

# Task especial para  a ia

- [ ] Criar doc de Como falar com as ias com simbolos ? ex: "_O símbolo padrão da matemática para "é diferente de" é o **`≠`** (==um sinal de igual com um corte diagonal==). Ele indica que dois valores ou expressões não são iguais. Exemplo: 5 ≠ 3 (cinco é diferente de três)" etc...
💡 Símbolos de Estrutura e Organização

Estes símbolos ajudam a LLM a entender onde começa e termina cada parte do seu comando.

- **`###` (Três cerquilhas / hashtags)**
    - **O que faz:** Cria títulos e subtítulos (formato Markdown).
    - **Por que usar:** Separa claramente os tópicos da sua instrução, como se fossem capítulos de um livro. [[1](https://itsanamelo.com.br/como-criar-bons-prompts-ao-usar-inteligencia-artificial/)]
- **`---\` (Três hifens)**
    - **O que faz:** Cria uma linha divisória horizontal no texto.
    - **Por que usar:** É excelente para separar o contexto principal da sua pergunta final.
- **`>` (Sinal de maior seguido de espaço)**
    - **O que faz:** Cria um bloco de citação (texto recuado).
    - **Por que usar:** Ideal para colar textos de outras fontes (como e-mails ou artigos) que você quer que a LLM analise ou resuma.

> -  

---

📌 Símbolos de Delimitação (Os mais importantes para LLMs!)

As LLMs funcionam prevendo a próxima palavra com base no contexto. Delimitadores servem como "paredes" para isolar informações importantes. [[1](https://imasters.com.br/inteligencia-artificial/desvendando-a-comunicacao-com-llms-o-poder-da-engenharia-de-prompts)]

- **`"""` (Três aspas duplas)**
    - **O que faz:** Isola blocos inteiros de texto ou instruções.
    - **Por que usar:** Evita que a IA confunda as suas ordens com o texto que está sendo analisado.
- **`` ` `` (Crase única) ou ` ``` ` (Três crases)**
    - **O que faz:** Destaca códigos de programação ou palavras-chave isoladas.
    - **Por que usar:** Diz para a IA: _"Trate o que está aqui dentro exatamente como texto literal, não mude nada"_.
- **`[ ]` (Colchetes)**
    - **O que faz:** Indica variáveis ou espaços para preenchimento.
    - **Por que usar:** Você pode dizer para a IA: _"Substitua o que está dentro de `[nome_do_cliente]` pelo nome real"_.

---

🔎 Por que utilizar esses símbolos especialmente com LLMs?

1. **Reduz a "Alucinação" (Erros):** Quando você separa o texto com símbolos claros, a IA tem menos chances de misturar as suas instruções com os dados fornecidos.
2. **Economiza palavras:** Em vez de escrever _"Por favor, considere o texto abaixo que começa na próxima linha e termina no fim do parágrafo como a base do resumo"_, você pode simplesmente escrever: `Analise o texto abaixo: """ [seu texto] """`.
3. **Melhora a formatação das respostas:** Se você iniciar o seu comando usando tópicos com hifens (`-`) ou títulos (`###`), a IA tende a espelhar a sua organização e responder de forma muito mais limpa e legível.

---

 
