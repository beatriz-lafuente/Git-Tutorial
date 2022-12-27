Olá, neste projeto você aprenderá alguns comandos do Git
# Como usar o Git e Github na prática

Olá sejam bem vindos, eu sou a Bia e neste repositório vou mostrar para vocês como utilizar o Git na prática.

## Workflow

![workflow](https://user-images.githubusercontent.com/121397357/209671168-8812a5b2-b13e-4502-8e7d-d4a113e28525.png)

## Instalar o Git
O primeiro passo é fazer a instalação do Git no seu computador através do link.
* [Link com os downloads](https://git-scm.com/downloads)

## Criar um novo projeto

Vou usar o meu repositório TutorialGit como exemplo para mostrar para vocês como criar um novo projeto. 
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

O comando `git add` é necessário antes de darmos o commit (explicar pq)

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

Para voltar ao branch principal `$ git checkout main` e para voltar depois ao branch `git checkout "nome_do_branch"` novamente

Mas e agora, como se junta o novo branch criado com o main?

## Merge

Através do merge!

* `$ git checkout main`

* `$ git merge "nome_do_branch"`

Desta forma todas as alterações feitas na branch `"nome_do_branch"` estão na `main`.

* E para finalizar `git push origin main` para atualizar o respositório do Github

## Clone

Como se pode fazer o download de um código?

Sempre que você entrar num epositório, seja o seu ou o de qualquer outra pessoa, terá esse botão `Code`, que quando você clica aparece um link:

<img src="https://media.discordapp.net/attachments/812313742192279612/836823564513705994/unknown.png">

* Você irá copiar esse link e levar ele lá pro nosso terminal

* O comando para puxar o projeto para a sua máquina é o `git clone https://github.com/rafaballerini/GitTutorial.git`

Não é necessário criar um repositório antes disso, como fizemos anteriormente com o `git init`. Dessa vez, basta abrir o terminal e clonar o projeto e tudo aparecerá!

## Pull

E se eu fizer uma alteração no repositório, como vocês podem atualizar na máquina de vocês?

* Basta vocês executarem o comando `git pull`, ele irá puxar todas as alterações feitas no repositório do Github para o seu repositório local

## Fork

Mas Rafa quando eu fiz o clone do seu repositório ele não apareceu no meu Github.
Existe a ferramenta `fork`, que é bem mais simples para fazer isso
Você só precisa apertar nesse botão dentro do repositório e TCHANAM! Ele aparece automaticamente lá na sua conta:

<img src="https://media.discordapp.net/attachments/831974152667398214/836826687634407434/unknown.png">

## Pull request

O último conceito que quero ensinar para vocês é o de Pull Request, vamos entender como ele funciona:

* Após você ter dado um fork no projeto e ele ter ido pra sua conta, você poderá alterar o projeto e adicionar as funcionalidades que deseja

* Você pode por exemplo dar um fork no meu repositório de `Formulário` para adicionar uma validação de campos ou qualquer outra coisa que acha válido

* Depois disso, você poderá salvar o projeto, dar o `git add .`, `git commit -m "validação de botões"` e `git push origin main`

Quando você for olhar o seu Github, verá que existe uma mensagem parecida com a seguinte:

<img src="https://media.discordapp.net/attachments/831974152667398214/838990983852458035/unknown.png">

Isso significa que a branch do seu repositório está 1 commit "na frente" da branch original

O que você deve perceber agora é esse botão que aparece em seguida:

<img src="https://media.discordapp.net/attachments/831974152667398214/838991711249235998/unknown.png">

Ele servirá para caso você deseje enviar para o dono do repositório original uma solicitação de pull, ou seja, fazer com que ele puxe as alterações que você fez no seu repositório para o repositório dele, original

Ao clicar nesse botão, você será direcionado para uma página que fará a avaliação se esse `pull request` terá conflitos ou não com o código no repositório original. Caso não tenha, bastão clicar no botão de `Create pull request`

<img src="https://media.discordapp.net/attachments/831974152667398214/838992584893399100/unknown.png">

Você irá colocar um nome intuitivo, que demonstre a funcionalidade adicionada e o ideal é que você também crie uma boa descrição do que desenvolveu, não somente explicando o que é, mas ensinando ao dono do repositório original a forma como ele poderá testar também

Depois disso, basta esperar para que o dono da branch original aceite o seu pull request

## Finalização

Existem diversas outras funcionalidades do Git e do Github, porém tenho certeza que com tudo isso que vocês viram hoje vocês já conseguem desenvolver um projeto de uma forma bem legal

Recomendo sempre vocês darem uma olhada na [documentação do Git](https://git-scm.com/doc), pois qualquer dúvida que apareça pode ser respondida por lá na explicação

**Não esqueçam de deixar o like e se inscrever no [canal do Youtube](https://youtube.com/RafaellaBallerini) ❤**

Até semana que vem, um beijo!








