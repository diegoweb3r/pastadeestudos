# Guia rápido de Git e GitHub

Um resumo dos comandos mais usados no dia a dia e um passo a passo para
criar um repositório no GitHub diretamente pelo terminal.

> **Git** é o sistema de controle de versão que roda no seu computador.
> **GitHub** é uma plataforma online onde você pode hospedar
> repositórios Git e colaborar com outras pessoas.

## 1. Configuração inicial

Faça essa configuração uma única vez em cada computador:

``` bash
# Define seu nome
git config --global user.name "Seu Nome"

# Define o e-mail associado à sua conta GitHub
git config --global user.email "seu-email@example.com"

# Confere as configurações
git config --global --list
```

Para conferir se o Git está instalado:

``` bash
git --version
```

## 2. Criar ou baixar um repositório

``` bash
# Inicia um repositório Git na pasta atual
git init

# Baixa um repositório que já existe no GitHub
git clone URL_DO_REPOSITORIO

# Exibe o endereço remoto configurado
git remote -v

# Adiciona um repositório remoto chamado origin
git remote add origin URL_DO_REPOSITORIO
```

## 3. Acompanhar alterações

``` bash
# Mostra arquivos modificados, novos e preparados para commit
git status

# Mostra as diferenças ainda não preparadas
git diff

# Mostra as diferenças já preparadas para commit
git diff --staged

# Adiciona um arquivo específico à área de preparação
git add nome-do-arquivo

# Adiciona todas as alterações da pasta atual
git add .

# Remove um arquivo da área de preparação, sem apagar seu conteúdo
git restore --staged nome-do-arquivo

# Descarta alterações locais ainda não preparadas (cuidado!)
git restore nome-do-arquivo
```

**Fluxo básico:** `git status` → `git add` → `git commit`.

## 4. Registrar alterações (commits)

``` bash
# Cria um commit com uma mensagem descritiva
git commit -m "Adiciona tela inicial"

# Altera o último commit (use com cuidado se já publicou)
git commit --amend

# Exibe o histórico de commits
git log

# Histórico resumido em uma linha por commit
git log --oneline

# Histórico com gráfico de branches
git log --oneline --graph --all
```

Boas mensagens de commit descrevem o que mudou, por exemplo:

-   `Adiciona validação ao formulário`
-   `Corrige responsividade do cabeçalho`
-   `Atualiza documentação do projeto`

## 5. Enviar e receber alterações do GitHub

``` bash
# Envia a branch atual para o remoto
git push

# Envia a branch main pela primeira vez e configura o upstream
git push -u origin main

# Baixa e integra alterações da branch remota atual
git pull

# Busca atualizações do remoto sem integrá-las
git fetch

# Envia os commits locais para o remoto
git push origin nome-da-branch
```

`git fetch` apenas busca as novidades. `git pull` busca e tenta
integrá-las à sua branch.

## 6. Branches (ramificações)

Branches permitem trabalhar em funcionalidades sem alterar diretamente a
branch principal.

``` bash
# Lista as branches locais
git branch

# Lista branches locais e remotas
git branch -a

# Cria uma branch
git branch nome-da-branch

# Cria e já muda para a nova branch
git switch -c nome-da-branch

# Muda para uma branch existente
git switch main

# Incorpora outra branch à branch atual
git merge nome-da-branch

# Exclui uma branch local já integrada
git branch -d nome-da-branch

# Publica uma branch no GitHub
git push -u origin nome-da-branch
```

Exemplo de fluxo para uma funcionalidade:

``` bash
git switch main
git pull
git switch -c feature/nova-funcionalidade

# Faça as alterações nos arquivos...

git add .
git commit -m "Adiciona nova funcionalidade"
git push -u origin feature/nova-funcionalidade
```

## 7. Desfazer ou guardar alterações

Atenção: alguns comandos abaixo podem descartar trabalho. Confira o
`git status` antes de executá-los.

``` bash
# Desfaz alterações locais em um arquivo não preparado
git restore nome-do-arquivo

# Retira um arquivo da área de preparação
git restore --staged nome-do-arquivo

# Cria um novo commit que desfaz um commit anterior
git revert HASH_DO_COMMIT

# Guarda temporariamente alterações ainda não commitadas
git stash

# Lista alterações guardadas
git stash list

# Recupera as alterações guardadas e as remove da lista
git stash pop

# Recupera as alterações sem removê-las da lista
git stash apply
```

Evite usar `git reset --hard` sem ter certeza: ele pode apagar
alterações locais definitivamente.

## 8. Arquivo `.gitignore`

O `.gitignore` informa ao Git quais arquivos e pastas não devem ser
acompanhados.

Exemplo comum para projetos JavaScript/React:

``` gitignore
# Dependências
node_modules/

# Arquivos de ambiente e segredos
.env
.env.*
!.env.example

# Builds
dist/
build/

# Logs
*.log
npm-debug.log*

# Arquivos do sistema/editor
.DS_Store
Thumbs.db
.vscode/
```

Crie o arquivo `.gitignore` na raiz do projeto, antes de adicionar os
arquivos ao Git sempre que possível.

> Se um arquivo já está sendo acompanhado pelo Git, adicioná-lo ao
> `.gitignore` não faz o Git parar de acompanhá-lo automaticamente.

## 9. Criar um repositório no GitHub pelo terminal

A maneira mais prática é usar o **GitHub CLI (`gh`)**, ferramenta
oficial de linha de comando do GitHub. Ela permite criar o repositório
remoto sem precisar abrir o navegador.

### Passo 1 --- Instalar o GitHub CLI

No Windows, usando `winget`:

``` powershell
winget install --id GitHub.cli
```

Depois da instalação, feche e abra novamente o terminal. Confira:

``` bash
gh --version
```

Se você já tem o Git instalado, não precisa instalá-lo novamente.

### Passo 2 --- Entrar na sua conta GitHub

``` bash
gh auth login
```

Responda às perguntas do assistente. Em geral, escolha:

1.  **GitHub.com**
2.  **HTTPS** (uma opção simples para começar)
3.  **Login with a web browser**

O terminal mostrará um código. Siga a instrução para abrir a página de
autenticação, informe o código e autorize o GitHub CLI.

Confira se a autenticação funcionou:

``` bash
gh auth status
```

### Passo 3 --- Abrir a pasta do projeto

No terminal, navegue até a pasta do projeto. Exemplo no Windows:

``` powershell
cd "C:\Users\SeuUsuario\Desktop\Portfolio\MeuProjeto"
```

Dica: no Explorador de Arquivos, você também pode abrir a pasta do
projeto e usar a opção de abrir o terminal nela.

### Passo 4 --- Inicializar o Git

Se o projeto ainda não tem Git:

``` bash
git init
```

Defina a branch principal como `main`:

``` bash
git branch -M main
```

Se o projeto já é um repositório Git, não precisa executar `git init`
novamente.

### Passo 5 --- Preparar e registrar os arquivos

Confira se existe um `.gitignore` e se ele exclui arquivos que não devem
ser publicados, como `node_modules` e `.env`.

``` bash
git status
git add .
git commit -m "Initial commit"
```

Se o Git avisar que não há nada para commit, confira o `git status`:
talvez os arquivos já estejam commitados.

### Passo 6 --- Criar o repositório no GitHub e publicar

Para criar um repositório **público** com o nome da pasta atual e enviar
o projeto:

``` bash
gh repo create --source=. --public --remote=origin --push
```

Para criar um repositório **privado**, use:

``` bash
gh repo create --source=. --private --remote=origin --push
```

O comando cria o repositório no GitHub, configura o remoto `origin` e
publica a branch e os commits locais.

Se quiser escolher o nome do repositório, informe-o no comando:

``` bash
gh repo create nome-do-repositorio --source=. --public --remote=origin --push
```

### Passo 7 --- Conferir se deu certo

``` bash
git remote -v
git status
gh repo view --web
```

O último comando abre a página do repositório no navegador.

## 10. Atualizar o projeto depois da publicação

Depois que o repositório já existe, o fluxo mais comum é:

``` bash
# 1. Confira o estado do projeto
git status

# 2. Prepare as alterações
git add .

# 3. Registre as alterações
git commit -m "Descreve a alteração"

# 4. Envie para o GitHub
git push
```

Se estiver trabalhando em equipe ou em mais de um computador, atualize
sua branch antes de começar:

``` bash
git pull
```

## 11. Cola rápida: o fluxo que você mais vai usar

``` bash
git status
git add .
git commit -m "Mensagem do commit"
git push
```

Para começar uma funcionalidade em uma branch:

``` bash
git switch main
git pull
git switch -c feature/nome-da-funcionalidade
```

Ao terminar:

``` bash
git add .
git commit -m "Adiciona nome da funcionalidade"
git push -u origin feature/nome-da-funcionalidade
```

------------------------------------------------------------------------

## Observações importantes

-   Não publique senhas, tokens, chaves de API ou arquivos `.env`.
-   O `git add .` adiciona alterações da pasta atual; confira o
    `git status` antes do commit.
-   Um commit é um registro local. Ele só chega ao GitHub quando você
    faz `git push`.
-   `origin` é apenas o nome convencional dado ao repositório remoto;
    não é um comando especial.
-   `main` costuma ser o nome da branch principal, mas um projeto pode
    usar outro nome.
