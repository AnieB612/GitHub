# GitHub

## Conceitos básicos e úteis sobre o GitHub e Passo a passo para utilizá-lo, nesta ordem a seguir

Plataforma para:

Salvar códigos e suas diferentes versões ao decorrer de um projeto. Versionamento de códigos.

Existem duas formas de salvar, famoso versionar, os códigos que é:

* Trazendo o código do GitHub
  
* Enviando para o GitHub o código local salvo na máquina 

((Resumindo não passa de uma grande núvem de salvamento e edição ))

### CONFIGURAÇÃO BÁSICA
___________________________

* Versão do Programa Instalado
  
  git --version

* Comando para ver as informações a respeito do GIT
  
  git config

* Configurar o nome
  
  git config --global user.name "anie"
  
* Configurar o email
  
  git config --global user.email y_anie@hotmail.com

### COMANDOS BÁSICOS
----------------------


* Comando para limpar o terminal
  
  Ctrl + l

  clear

* Lista todos os arquivos e pastas que há dentro de uma pasta
  
  ls

* Volta pastas
  
  cd ..
  
* Cria um arquivo vazio tipo MD
  touch README.md 

###  CRIANDO UMA PASTA QUE SE DESEJA TRANSFORMAR EM UM REPOSITORIO GIT 
_______________________________________________________________________

* Criando uma pasta/diretorio
  
  mkdir + ( nome criado )

* Criando um repositório GIT, em main
  
  git init + ( nome criado )

  Cria um repepositorio GIT , nao é um repositorio GitHub, apenas cria esse repositorio no 
  programa GIT , este que podera fazer mudanças, e enviar dps para o GitHub depois.

* Para entrar/mudar para dentro do diretorio local
  
  cd .git

  Desde já e importante salientar que tudo que tem .git é porque esta escondido, assim sendo, 
  só é possivel ver as pastas que não sao visiveis mas estam ali, que sao os arquivos 
  responsaveis pelo controle de versao.

* Ver as informaçoes da pasta, do servidor de onde foi clonada e demais dados
  
   cat config (dentro da pasta cd .git)

* Ver todos os repositórios remotos ao qual voce esta vinculado

  git remote -v  ( dentro de cd .git)

  CASO NÃO ESTEJA FAZ-SE ISSO:
  
  É necessário estar conectado a um repositóro remoto GITHUB, se não estiver precisa ser 
  efetuado o passo a seguir:

* ### ***Conexao entre o repositório local e remoto:***

  git remote add origin + ( url do repositorio remoto )

  Repositorios vinculados entre si

  A partir de um REPOSITORIO LOCAL - Git, conectar a um servidor, um REPOSITORIO REMOTO - 
  GitHub

### COPIANDO UMA PASTA/REPOSITÓRIO NO GITHUB NA QUAL SE DESEJA TRANSFORMAR EM UM REPOSITORIO GIT LOCAL
_______________________________________________________________________________________________

* Pasta a ser copiada do github para o computador
 
  git clone + ( link da pasta )

   Clona um repositorio remoto do GitHub  para o seu computador

* Utiliza-se para mudar o nome da pasta que se clona do GitHub
  
   git clone + ( link da pasta ) + nome que quer chamar a pasta

* Informaçoes da pasta

   cat config ( dentro de cd .git)

* Ver todos os repositorios remotos ao qual voce esta vinculado

   git remote -v  (dentro de cd .git)

*Obs.: 

oring = nome padrao do servidor de onde a gente clonou a pasta


### SALVANDO ALTERAÇÕES NO REPOSITORIO LOCAL
___________________________________________________

* Criando uma pasta/Diretorio
   mkdir + ( nome criado )

* Dentro da pasta criada em main
   git init

OU

* git init + ( nome criado )

* Ver o estado da area de preparação
  git status

  Detecta as alterações em um arquivo e avisa se está pronto para ser salvo
  Vê o status da arvore de preparação
  NÃO DECTA ARQUIVO VAZIO (.git)

**TOUCH/ECHO** - cria arquivos 

touch + ( qualquer coisa ) ... ele cria 
touch (arquivo md) porem nesta nova pasta criada por ultimo, ex.: resumos/resumos.md

touch README.md = cria um arquivo vazio tipo MD

ECHO - criaçao de arquivos, pode ser MD tmb

echo "#commit-1-branch-main" ( assunto que estara dentro da pasta ) > commit-1-branch-main.txt ( nome que sera salvo )

echo "# oi gososa " > commit-2-branch-main.txt


  Dentro de main/pasta:
  
* Adiciona o arquivo para a area de preparação
  git add + ( nome do arquivo )

  NADA está salvo, só estará salvo quando for feito o commit , aqui É APENAS area de preparação para o salvamento

  - **git add** .

  Para mandar vários arquivos ao mesmo tempo para a area de preparação

  **COMMIT**

  Dentro da pasta criada faz / main: 

   git status ( ver se está tudo ok ...) 

  * PARA FAZER O COMMIT ( salvar na nuvem )

    git commit -m " mensagem com a descrição do que aquele commit "

    O  Commit captura um instantâneo das mudanças preparadas do projeto no momento

  * Informações sobre o commit feito e o hash ( identidade do commit )

    git log

    git status ( tem de estar tudo ok , e sem commits a serem feitos )

    mkdir  nova pasta

    git status

    echo "#commit-1-branch-main" ( assunto que estara dentro da pasta ) > commit-1-branch- 
    main.txt ( nome que sera salvo )

    git status

  * Arquivos que nao devem ser mostrados

    gitignore

    - echo + ( nome da pasta ) + > .gitignore 
    - echo resumos/ > .gitignore ( exemplo )
    Existem arquivos que nao devem ser mostrados ou tampouco enviados para o commit 
    Se faz isso para que a pasta resumos va para lá e nao atrapalhe
    mas o git ignore ira aparecer no status sempre do git status e usado sempre que nao quiser 
    que um arquivo seja salvo


    se tirar o resumos/ ele volta a aparecer:
    - echo > .gitignore
     ele volta a ser reconhecido, rastreavel , UNtracked files
     mas a pastinha git ignore vai existir la nos arquivos

     
    gitkeep
    
    - touch + ( nome do arquivo ) +/ .gitkeep
    - touch aulas/.gitkeep
    diretorio bastante comum
    utilizado para que o git reconheça um diretorio vazio


###  DESFAZENDO ALTERAÇÕES NO REPOSITÓRIO LOCAL
______________________________________________________________

Supondo que já foi feito um GIT INIT em uma pasta, dentro de main:

*  Desfaz o comando do git init e seu conteudo, deixa de indicar a branch main

  rm -rf .git

* Quando foi feito algo errado OU apagou alguma coisa errada e necessita voltar ao ponto que se estava antes:

 git restore + ( nome do arquivo )
 git restore README.md

* Quando se necessita mudar a mensagem de um COMMIT

  git commit --amend -m"nome da mensagem"
           
                    OU 

  git commit --amend
  
   Abre o editor
   i = inserir mensagem
   Sair do editor 
   Esc:wq

* Para Apagar COMMITS ou Retornar COMMITS
 
RESET - PARA RETORNAR COMMITS 

- git reset ( -- soft / -- mixed / -- hard )
    3 opcoes de desfazer um commit
   
SOFT:
     copia a hash com o git log git log
     git reset -- soft + ( hash ) 
     git reset --soft 46a4fd19cedf9a9897d37ca938bd647b8b804e20
     basicamente pegou o ultimo commit, nao o primeiro (HEAD)
     nesse caso,  ele voltou para a area de preparaçao 


MIXED:
     git reset -- mixed + ( hash )
     nesse caso, usou a hash do "soft" 
     basicamente voltou a um ponto alem do soft , mais distante , nesse caso
 
     
HARD:
     git reset -- hard + ( hash )
     usou a hash do ultimo commit feito
     voltou ao ponto do primeiro commit, o commit inicial, pois usou a hash do "mixed", assim nao sobrando nada 


RESET - PARA EXCLUIR ARQUIVOS

- git reset + pasta e nome do arquivo ou git reset + nome do arquivo ( caso ja estiver na pasta)

 git reset resumos/aula1.md

             OU

 git restore --staged resumos/aula2.md ou  git restore --staged aula2.md

* Histórico das alterações realizadas
   git reflog

### ENVIANDO E BAIXANDO ALTERAÇÕES COM O REPOSITORIO REMOTO
-----------------------------------------------------------------------

- Enviando as alterações de um repositório existente pelas linhas de comando

- git status
- git add .
- git commit -m""
- git status
- git log


* Enviando para o git:

  git remote add origin + ( url do repositorio remoto )

  Conexao entre o repositorio local e remoto
  Repositorios vinculados entre si
  A partir de um REPOSITORIO LOCAL (conectar) a um servidor, um REPOSITORIO REMOTO ( GIT )

  obs.: observar a branch que voce está, assim sendo , como ja esta dentro da main, será
  realizado um comando git push;

  
* Comando responsavel por levar as modicicações do repositorio local para o repositorio remoto

  git push

  Obs.: quando se está utilizando o github, é so apertar " . " que abre um editor online 
      la tem que salvar com o " + " e dps com fazer o commit e push

**PARA SALVAR AS MUDANÇAS NO COMPUTADOR**

Comando responsavel por puxar as alteraçoes do repositório remoro e mesclar com as informações do repositorio local

git pull

 ### TRABALHANDO COM BRANCHES - CRIANDO, MESCLANDO E DELETANDO 
-------------------------------------------------------------------------------------------
                  
- BRANCH

* É uma ramificação, um  " galho ", do seu projeto

* Feita para testes , funcionalidades novas que nao temos certeza se será isso ou nao, MAS, sem afetar a branch principal (main);

* É um norte para o seu commit;

* É um ponteiro do commit no histórico do repositório;

          branch (main ) -> commit 2 -> commit 1 -> commit 0

* Ao se criar uma nova branch , ela será a cópia do que existiu , com a main, mas de forma isolada neste universo

         branch (test) aponta para os mesmos commits anteriores:

         branch (test ) -> commit 2 -> commit 1 -> commit 0

* Mas se for realizado um novo commit na branch test , esse ficará nesta branch, apenas 

        branch (test ) -> commit 3 -> commit 2 -> commit 1 -> commit 0

* Para juntar o commit 3 da branch test com o a branch main , que esta no commit2 , é necessario fazer uma mescla

* Cria uma nova Branch
  
git checkout -b ( nome da nova branch )

git checkout -b teste
     
* Sai da branch que se está e entra na outra que se quer estar 
  
git checkout + ( nome da branch )

git checkout main

* Lista todos os ultimos commits efetuados
  
git branch -v

* União de duas Branchs
  
git merge + ( nome da branch que se quer mesclar com a main )

git merge teste

* Lista todas as branches existentes no repositorio
  
git branch 

* Exclui uma branch
  
git branch -d + ( nome da branch a ser excluida )

git branch -d teste

### CONFLITOS DE REPOSITORIO LOCAL X REMOTO
--------------------------------------------------------

- git remote -v  ( dentro de cd .git)
    ver todos os repositorios remotos ao qual voce esta vinculado 

- git push ( vai dar erro ...)
  
- git pull ( vai baixar as alterações e juntar , tipo um merge )
  
 faz a modicação no arquivo que vc quer ...

- git status ( irá mostrar essas modificações )
  
-git add .

- git commit -m " mensagem "
  
- git log
  
- git push

  
### OUTROS RECURSOS EXTRAS
_______________________________


COMANDOS PARA BAIXAR O CONTEUDO DE UMA BRANCH REMOTA SEM MESCLAR COM O CONTEUDO DA BRANCH LOCAL

git fetch: para baixar as alterações sem mesclar com o repositorio local
baixar as alterações do repositorio origin da branch main

git fetch origin main
 

git diff: ver as diferenças entre a branch main e a branch origin

git diff main origin/main

se quiser trazer as alterações do repositorio remoto para o repositorio local:

git merge origin/main

utilizado para copiar apenas uma branch :

git clone + ( url do repsositorio remoto ) + --branch + (nome da branch) --single-branch

git stash - modificalçoes que foram feitas ele arquiva -- ( complicado )

  
  
  


    

  


  



  
  

  



  
  

  

  
  
  


  

  
  


  
  












