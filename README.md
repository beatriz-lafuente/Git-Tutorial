Olá, neste projeto você aprenderá alguns comandos do Git
# Como usar o Git e Github na prática

Olá sejam bem vindos, eu sou a Bia e neste repositório vou mostrar para vocês como utilizar o Git na prática.

## Workflow

![workflow](https://user-images.githubusercontent.com/121397357/209671168-8812a5b2-b13e-4502-8e7d-d4a113e28525.png)

## Instalar o Git
O primeiro passo é fazer a instalação do Git no seu computador através do link.
* [Link com os downloads](https://git-scm.com/downloads)

## Criar um novo projeto

Vou usar o meu repositório TutorialGit como exemplo para mostrar como criar um novo projeto. 
Depois de instalar o Git o segundo passo é:

* Criar uma nova pasta no seu PC com o nome `TutorialGit`

* Abrir o VSCode nessa pasta

* Criar um novo arquivo `README.md`

* Escrever dentro dele `Olá, neste projeto você aprenderá alguns comandos do Git`

* Salvar o arquivo

E agora, começamos a utilizar o Git.

## Git

* Abrir o Git Bash que foi instalado no computador

![gitbash](https://user-images.githubusercontent.com/121397357/209668647-6efb0668-97ad-4424-89f7-68b8daf6493e.png)

Escrever os seguintes comandos no GitBash:

* `$ git init` para inicializar o repositório

Foi criada uma pasta `.git` e é ali que toda a magia acontece, então não apague

* `$ git add README.md` para colocar o arquivo na área de stagging

<img src="https://i1.wp.com/www.markus-gattol.name/misc/mm/si/content/git_git_add.png">

O comando `git add` é necessário antes de fazer o commit

* `$ git commit -m "add readme.md"` para dar de facto o commit no repositório

* `$ git branch -M "main"` para alterar o nome da branch principal de `master` para `main` (é uma boa prática atualmente recomendada)

Recebemos a confirmação de que o commit aconteceu! Podemos continuar.

## Repositório no Github

Aqui vou mostrar como usar o Github.

* Depois de criar conta na plataforma, clique em `New` para criar novo repositório

![new_repository](https://user-images.githubusercontent.com/121397357/209675373-01c1e926-d573-4404-a599-e07260666f96.png)

Depois de preencher com as informações do projeto, dar o nome do repositório e colocar uma breve descrição clique em `Create repository`

* Para passar o commit do repositório local (da sua máquina) para um repositório na plataforma do Github, utilize o comando `$ git remote add origin <link do repositório>`. No meu caso, o link é https://github.com/beatriz-lafuente/TutorialGit.git

![link_github](https://user-images.githubusercontent.com/121397357/209676821-b1ebfdee-275d-42b3-9376-56b7d979fc54.png)

* `origin` é o nome utilizado para referenciar o repositório criado

O repositório local já está conectado com o respositório do Github, porém o `commit` que foi feito na máquina não vai automaticamente para a plataforma

* Para isso é necessário empurrar, enviar para lá utilizando o comando `$ git push -u origin main`

Agora se recarregar a página irá ver o arquivo aqui na plataforma!

## Alterar e adicionar arquivos

Caso alterações sejam feitas no arquivo ou caso a sua intenção seja adicionar um novo arquivo é necessário subir essas alterações.

Para isso utiliza-se:

* `$ git add .` (o ponto `.` adiciona todos os arquivos)

* `$ git commit -m "add changes"`

* Lembrando que para alterar algo no respositório do Github é preciso dar o push, então `$ git push origin main` (desta vez, sem o `-u` uma vez que já estamos conectados)

## Branch

* Para adicionar um novo branch `$ git checkout -b "nome_do_branch"`
Este comando além de criar o branch entra nele com o checkout.

* Depois fazer o `$ git add .` e commit `$ git commit -m "add new files"` para as alterações feitas

* Para enviar as alterações feitas para o novo branch `$ git push origin "nome_do_branch"`

Agora se olharmos para o Github, veremos que tem 2 branches, `main` e `"nome_do_branch"`

Para voltar ao branch principal `$ git checkout main` e para voltar depois ao branch `$ git checkout "nome_do_branch"` novamente

Mas e agora, como se junta o novo branch criado com o main?

## Merge

Através do merge!

* `$ git checkout main`

* `$ git merge "nome_do_branch"`

Desta forma todas as alterações feitas no branch `"nome_do_branch"` estão no `main`.

* E para finalizar `$ git push origin main` para atualizar o respositório do Github

## Clone

Como se pode fazer o download de um código?

Sempre que entrar num repositório, seja o seu ou o de qualquer outra pessoa, terá o botão `Code`, que quando você clica aparece um link:

![link_github](https://user-images.githubusercontent.com/121397357/209736505-4ae96201-553b-47e3-9c58-868df0e49113.png)

* O primeiro passo é copiar esse link e abrir a terminal do GitBash

* E usar o seguinte comando `$ git clone link_copiado` para puxar o repositório para a sua máquina

## Pull

E se for feita uma alteração no repositório, como pode atualizar o repositório no seu computador?

* Basta executar `$ git pull` para puxar todas as alterações feitas no repositório do Github para o seu repositório local

## Fork

E se quiser ter o código de outro utilizador do GitHub a aparecer no seu perfil?

O `fork` é utilizado de forma a copiar o repositório de outro utilizador do GitHub e a aparecer no seu perfil para próprio uso.

* Basta clicar no botão `Fork` dentro do repositório e pronto! Ele aparece automaticamente na sua conta do GitHub:

![fork](https://user-images.githubusercontent.com/121397357/209737841-713501c3-b64a-42fe-b30c-6920fc28245c.png)

## Pull request

O Pull Request funciona da seguinte forma:

* Após ter feito `fork` num repositório e esse repositório estar disponível na conta do GitHub, é possível alterar o projeto e adicionar funcionalidades se desejar

* Depois de feitas as alterações, e de guardar o projeto, utiliza-se os comandos `git add .`, `git commit -m "novas alterações"` e `git push origin main`

Caso você deseje enviar para o dono do repositório original uma solicitação de pull, ou seja, fazer com que ele puxe as alterações que você fez no seu repositório para o repositório dele (original) deve clicar nos botões:

* `Open pull request`
ao clicar neste botão, será direcionado para uma página que fará a avaliação se esse `pull request` terá conflitos ou não com o código no repositório original

* Caso não tenha, bastão clicar no botão `Create pull request`

Boas práticas incluem pôr um nome intuitivo, que demonstre a funcionalidade adicionada e o ideal é também criar uma boa descrição do que foi desenvolvido, não somente explicar o que é, mas ensinar ao dono do repositório original a forma como ele poderá testar também.

Depois basta esperar que o dono do branch original aceite o pull request!

## Conclusão

Existem muitas outras funcionalidades do Git e do Github! 
Espero com este tutorial ter conseguido ajudar vocês a criar um repositório Git e a utilizar o GitHub para desenvolverem os vossos projetos.

Ver a documentação do Git ajuda sempre, pois qualquer dúvida que apareça pode ser respondida lá

Não se esqueçam de deixar uma estrela se gostaram e se foi útil ❤
