# Curso GIT e GITHUB

## Git
- sistema de controlo de versões
- documenta e armazena todas as alterações do projeto

## GitHub
- rede social de projetos
- hospedar e partilhar projetos

Vantagens: backup, controlo de versoes(qualquer alterações no codigo), trabalhar em equipa(integração), portfolio

Para criar funcionalidades - criar outro ramo sem interferir no ramo principal e depois fundir
HEAD - ponto onde o projeto se encontra - ultimo commit

## Comandos basicos
- git version (ver versao)
- git config --global user.name "Name"
- git config --global user.email "email@gmail.com"
- git config user.name (ver nome)
- git config core.editor (ver editor)
- git config --global core.editor " " (mudar editor)
- pwd (localização)
- cd /c (entrar em c)
- ls (listar ficheiros)
- ls -a (listar ficheiros ocultos)
- mkdir (criar diretorio)
- touch (criar ficheiro)

## Comandos iniciais
- git init (criar repositorio local)
- git status (ver arquivos novos ou modificações feitas)
- git add . (adicionar todos os arquivos novos e modificados ao container)
- git commit -m "Criado os arquivos a.txt b.txt" (Comentario relativamente ao add .) 
- git log (ver historico de commits)
- git log --oneline (ver historico simples)
- git log --graph (ver desenho do grafo de commits)
- git log --oneline --graph (ver historico simples com desenho do grafo)
- git log --oneline --graph --all (ver historico simples com desenho do grafo com todos os ramos)
- git log --graph --all (ver desenho do grafo de commits com todos os ramos)
- git commit -am "a.txt adicionei a linha entender o head" (adicionar e fazer commit)

## Comandos de commits
- git branch (ramo em que o projeto se encontra) - UTIL
- git checkout 5cfc1ad (recuperar para uma versao anterior - apontar o head para o respetivo commit 5cfc1ad)
- git checkout master (desfazer a recuperação e retornar à ultima versao)
- git diff (ver revisao do que foi adicionado e apagado)
- git checkout a.txt (anular alterações recentes a um ficheiro)
- git reset HEAD (remover add. do container - o ficheiro fica igual)
- git reset --hard a2f2800 (remover um commit e passar para o commit: a2f2800)

## Comandos de ramos
- git checkout -b teste (criar novo ramo e trabalhar sobre ele)
- ...agora basta modificar os ficheiros e dar add . e commits....
- git checkout master (retornar ao ramo master)
- ...agora basta modificar os ficheiros e dar add . e commits....
- git merge teste (unir ramo teste ao ramo master - é preciso estar no ramo master)
- git merge --abort (cancelar união no caso de gerar conflito)

## Caso dê erro a unir
- corrigir conflitos manualmente
- git add .
- git commit -m "Fusão dos ramos e resolucao do conflito a.txt"

## Criar repositório remoto no GitHub e enviar os ficheiros(se já existir localmente)
- git remote (verifica se existe repositório remoto)
- Aceder ao github.com e criar o Repositório no botão +
- Tirar o visto em "Initialize this repository with a README"
- git remote add origin https://github.com/oliveirasmj/git.git (copiar o link do git)
- git remote (verifica se existe repositório remoto)

## Enviar ficheiros para o GitHub
- git push -u origin master (enviar dados para o GitHub)
- OU
- git push

## Atualizar ficheiros para repositorio local
- git pull

## Clonar o repositório para o windows
- git clone https://github.com/oliveirasmj/git.git

## Quando push dá erro
- git fetch (download das alterações que estão no repositório para fazer análise do que foi modificado e resolver problemas de conflito)
- git checkout origin
- git checkout master
- git pull (atualizar tudo para local para resolver os problemas)
- git add .
- git commit -m "conflito resolvido"
- git push

## Git Fork
- Significa que acabaste de criar uma cópia do repositório principal de um código-fonte do projeto no teu próprio perfil do GitHub. 
- Aqui tu podes experimentar o que quiseres sem afetar a principal fonte desse projeto.
- 1)Selecionar o projeto no github
- 2)Clicar em Fork
- 3)Ir a "Your repositories" e clicar no projeto
- 4)O Projeto está clonado no perfil do teu github
- 5)Adicionar as alterações que achas necessário no projeto
- 6)Fazer o commit
- 7)Clicar em "New Pull Request" e depois em "Create Pull Request"

## Pull Request
- Serve para solicitar uma alteração ao projeto original. O criador será solicitado podendo ou não aceitar a alteração.
- O outro utilizador para aceitar deverá entrar no projeto e para aceitar:
- 1)Clicar em "Merge pull request"
- 2)e clicar em "Confirm merge"

## Instalar no linux
- sudo apt-get update
- sudo apt-get install git
