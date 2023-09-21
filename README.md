                                                                              #GitHub 
                                                                          ________________

# Conceitos básicos e úteis sobre o GitHub

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
_____________________

* Comando para limpar o terminal
  
  Ctrl + l

  clear

* Lista todos os arquivos e pastas que há dentro de uma pasta
  
  ls

* Volta pastas
  
  cd ..

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

* Conexao entre o repositorio local e remoto:

  git remote add origin + ( url do repositorio remoto )

  Repositorios vinculados entre si

  A partir de um REPOSITORIO LOCAL - Git, conectar a um servidor, um REPOSITORIO REMOTO - 
  GitHub

  

  

  
  
  


  

  
  


  
  












