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
- git config --global core.editor " " (mudar editor - colocar caminho do editor entre aspas)
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

## Kit primeiros socorros
- git clean -df - (desfazer tudo desde o último commit - reverter ficheiros) - CONVEM FAZER O COMANDO ABAIXO DESTE
- git checkout -- . (desfazer tudo que eu fiz desde o último commit - apagar arquivos e pastas)
- git reset --soft HEAD~1 (remover o último commit, porém mantendo os arquivos como estão)
- git reset --hard HEAD~1 (remover o último commit inclusive as alterações nos arquivos)
- git push -f origin HEAD^:master (apagar o último commit no Github)
- git reset --hard a2f2800 (remover commits e retorna ao commit a2f2800)

- git checkout 5cfc1ad (recuperar TEMPORARIAMENTE para uma versao anterior - apontar o head para o commit 5cfc1ad - nao editar codigo, caso contrário para depois sair do temporario fazer os dois comandos de desfazer tudo desde o último commit)
- git checkout master (voltar ao último commit - sair do TEMPORARIO apontar o head para o master)

- git reset HEAD (remover add. do container - o ficheiro fica igual)
- git checkout a.txt (anular alterações recentes a um ficheiro)
- git diff (ver revisao do que foi adicionado e apagado)
- git branch (ramo em que o projeto se encontra) - UTIL

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

## Criar repositório remoto no GitHub(se já existir localmente)
- git init (criar repositorio local)
- git remote (verifica se existe repositório remoto)
- Aceder ao github.com e criar o Repositório no botão +
- Tirar o visto em "Initialize this repository with a README"
- git remote add origin https://github.com/oliveirasmj/git.git (copiar o link do git) - associa o repositório local ao remoto
<p> <p>
- ATENCAO : Fazer este comando (git pull origin master) APENAS SE criou o "gitignore" no GitHub - às vezes, há arquivos sensíveis (exemplo: senhas) ou que são irrelevantes e que não se deseja versionar (exemplo: node_module)

## Enviar ficheiros para o GitHub
- (git add .)
- (git commit -m "Projeto criado")
- git push -u origin master (o primeiro push de um repositório deve conter o nome do repositório remoto e o branch)
- git push (os outros pushes não precisam da informação acima)

## Atualizar ficheiros para repositorio local
- git pull

## Clonar o repositório para o windows (se não existir localmente)
- git clone https://github.com/oliveirasmj/git.git

## Quando push dá erro
- git fetch (download das alterações que estão no repositório para fazer análise do que foi modificado e resolver problemas de conflito)
- git checkout origin
- git checkout master
- git pull (atualizar tudo para local para resolver os problemas)
- git add .
- git commit -m "Conflito resolvido"
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

## Diferença entre: “git add --all”, “git add .” e “git add -u”
https://pt.stackoverflow.com/questions/326160/diferen%C3%A7a-entre-git-add-all-git-add-e-git-add-u
