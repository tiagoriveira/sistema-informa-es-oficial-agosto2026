# Comandos e Atalhos Windows — Produtividade

> Nota pessoal solta, não é KNOWLEDGE nem segue formato PARA — fica na raiz por pedido do
> Tiago em 2026-08-19, "por hora". Pode virar RECURSOS mais pra frente.

## Windows geral

| Atalho | Ação |
|---|---|
| `Win + E` | abrir Explorador de Arquivos |
| `Win + D` | mostrar área de trabalho |
| `Win + L` | bloquear tela |
| `Win + Tab` | visão de tarefas (janelas + desktops virtuais) |
| `Win + Ctrl + D` | criar novo desktop virtual |
| `Win + Ctrl + →` / `←` | trocar de desktop virtual |
| `Win + Ctrl + F4` | fechar desktop virtual atual |
| `Win + V` | histórico da área de transferência (ativar 1x em Configurações → Sistema → Área de Transferência) |
| `Win + Shift + S` | recorte de tela (captura parcial) |
| `Alt + Tab` | trocar janela ativa |
| `Win + número` | abrir/focar o app fixado na barra de tarefas na posição N |
| `Win + →` / `←` / `↑` / `↓` | encaixar janela (snap) na metade/canto da tela |
| `Win + Shift + →` / `←` | mover janela pro monitor ao lado (multi-monitor) |
| `Win + .` | abrir painel de emojis/símbolos |
| `Win + I` | abrir Configurações |
| `Win + R` | abrir "Executar" (rodar comando/programa direto) |
| `Win + X` | menu rápido (Gerenciador de Dispositivos, PowerShell, Configurações etc.) |

## Explorador de Arquivos

| Atalho | Ação |
|---|---|
| `Ctrl + Shift + N` | nova pasta |
| `F2` | renomear |
| `Alt + ↑` | subir um nível de pasta |
| `Ctrl + L` | editar caminho direto na barra de endereço |
| `Ctrl + Shift + E` | expandir até a pasta atual na árvore lateral |
| `Alt + Enter` | propriedades do arquivo/pasta selecionado |
| Digitar caminho na barra de endereço + Enter | navegação rápida sem clicar em nada |
| `Ctrl + Roda do mouse` | mudar tamanho dos ícones |

## Terminal / PowerShell

| Atalho/comando | Ação |
|---|---|
| `Ctrl + R` | busca reversa no histórico de comandos (PSReadLine, PowerShell 7+) |
| `↑` / `↓` | navegar histórico de comandos |
| `Tab` | autocompletar caminho/comando |
| `Ctrl + C` | cancelar comando em execução |
| `cls` ou `Ctrl + L` | limpar tela |
| `Get-Content arquivo -Tail 20` | equivalente a `tail` |
| `Get-Content arquivo -Wait -Tail 10` | equivalente a `tail -f` (acompanhar log em tempo real) |
| `Get-ChildItem -Recurse -Filter "*.md"` | equivalente a `find` para arquivos |
| `Select-String "termo" *.md` | equivalente a `grep` |
| `Select-String "termo" -Path *.md -Recurse` | grep recursivo |
| `(Get-Content arquivo \| Measure-Object -Line).Lines` | equivalente a `wc -l` |
| `Measure-Command { comando }` | medir quanto tempo um comando leva |
| `Ctrl + Shift + T` (Windows Terminal) | nova aba |
| `Ctrl + Tab` (Windows Terminal) | trocar de aba |
| `Ctrl + Shift + D` (Windows Terminal) | duplicar aba atual (mesma pasta) |
| `notepad $PROFILE` | abrir o arquivo de perfil do PowerShell (pra criar alias/função permanente) |

**Alias úteis pra colocar no `$PROFILE`** (perfil do PowerShell, carrega toda sessão nova):
```powershell
function vault { Set-Location "C:\Users\tiago\OneDrive\Desktop\Sistema-de-estudos-tiago-agosto-2026" }
function gs { git status }
function gp { git pull }
```
Depois de editar o `$PROFILE`, rode `. $PROFILE` pra recarregar sem fechar o terminal.

## Git (uso no vault)

| Comando | Ação |
|---|---|
| `git status` | o que mudou, o que não está commitado |
| `git pull` | trazer o que a auditoria semanal na nuvem escreveu |
| `git add <arquivo>` | adicionar arquivo específico (evite `git add -A` sem olhar o status antes) |
| `git commit -m "mensagem"` | commitar |
| `git push` | subir pro remoto |
| `git log --oneline -10` | últimas 10 commits, uma linha cada |
| `git diff` | o que mudou, linha a linha, ainda não commitado |

## Claude Code CLI

| Atalho/comando | Ação |
|---|---|
| `Esc` | interromper a resposta atual |
| `Ctrl + C` (2x) | sair da sessão |
| `/clear` | limpar contexto da conversa atual |
| `/help` | ajuda sobre uso do Claude Code |
| `Shift + Tab` | trocar modo de permissão (plan/auto/etc., depende da versão) |
| `↑` | reusar/editar mensagem anterior enviada |

## Obsidian (uso no vault)

| Atalho | Ação |
|---|---|
| `Ctrl + O` | busca rápida de arquivo por nome |
| `Ctrl + Shift + F` | busca de texto em todo o vault |
| `Ctrl + P` | paleta de comandos (a porta de entrada pra quase tudo) |
| `Ctrl + N` | nova nota |
| `Ctrl + E` | alternar entre modo de edição e leitura |
| `Ctrl + G` | abrir visualização de grafo |
| `[[` | começar link pra outra nota (autocompleta) |
| `Ctrl + Clique` num link | abrir em nova aba sem sair da atual |
