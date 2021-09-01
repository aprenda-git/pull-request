# Pull request

Esse tutorial é um passo a passo prático de como enviar seu primeiro pull request, ao final você irá submeter um arquivo de _assinatura_ que ficará gravado aqui e servirá como prova de que você entendeu o processo e que fez de fato todos os passos aqui descritos.

Se você ainda tem dúvidas do que exatamente é um pull request ou para que ele serve, você pode acessar [aqui](https://docs.github.com/pt/github/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests) para ler mais sobre.

Caso você identifique um erro neste tutorial e queira submeter uma alteração, saiba como [aqui](contributing)

# 0 - Pegue seu garfo e faça um Fork

O passo 0 de qualquer pull request é identificar o repositório no qual você irá submeter seu código e criar um [Fork](https://docs.github.com/pt/get-started/quickstart/fork-a-repo). No caso desse tutorial o repositório em questão é esse aqui mesmo

<p align="center">
  <img src="https://raw.githubusercontent.com/aprenda-git/pull-request/define-tutorial-inicial/imagens/fork.gif">
</p>

Um Fork, de forma resumida, é uma cópia de um repositório para o **seu** perfil que mantém um apontamento para o repositório no qual se originou.
Dessa forma você tem uma cópia do repositório que irá trabalhar em seu próprio perfil podendo _commitar_ código aonde quiser, ou quase isso.

Você pode realizar um Fork desse repositório clicando no botão escrito Fork no canto superior direito da página (bem em baixo da sua foto de perfil) ou clicando [aqui](https://github.com/aprenda-git/pull-request/fork).

Selecione o perfil para o qual o repositório será _forkado_ e pronto.

# 1 - Clone o repositório _forkado_

Após o processo de fork o repositório em questão deverá aparecer na sua lista de repositórios pessoal. Note que ao invés de `aprenda-git/pull-request` o repositório carregará **seu** nome `seuNome/pull-request` pois afinal agora ele _pertence_ a você.

<p align="center">
  <img src="https://raw.githubusercontent.com/aprenda-git/pull-request/define-tutorial-inicial/imagens/forked.png">
</p>

Realize um clone desse repositório para sua máquina com o seguinte comando via `git cli`.

`git clone https://github.com/seuNome/pull-request`

Note que `seuNome` **precisa** ser substituido por seu _nick_ aqui do GitHub

# 2 - Crie uma branch para realizar as alterações.

Com o repositório devidamente clonado para uma pasta em sua máquina, navegue para dentro do mesmo utilizando seu terminal favorito.

Para que o processo de pull request seja executado de forma _isolada_ do restante da base de código, é importante que seja criado uma [branch](https://docs.github.com/pt/github/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-branches) separada.

Para isso rode o comando:

`git checkout -b nome-da-sua-branch`

O nome da sua branch fica por sua escolha, no mundo real as branches carregam um nome expressivo que indica o que está sendo feito na mesma, mas para os fins desse tutorial você pode ser criativo.

O comando `git checkout -b` deve criar uma nova branch e automaticamente te mover para dentro da mesma. Pronto, você ja pode começar a fazer alterações nos arquivos.

# 3 - Deixe sua marca.

Navegue até a pasta `pull-request/assinaturas` e lá dentro crie um arquivo do tipo [markdown](https://www.markdownguide.org/getting-started/). O arquivo leva seu nome e um número randômico (definido por você) de 4 dígitos separados por traço. Um exemplo seria:

`Ex: carlosguttemberg-0042`

Dentro desse arquivo você pode mandar o que quiser, mas caso falte imaginação, você pode seguir o seguinte modelo:

```markdown
Nome: Carlos Guttemberg

Comida favorita: Hamburguer :hamburger:

Aprendendo: Node, React

Sobre: Aqui você pode colocar mais informações sobre você caso queira. Se você é do tipo tímido(a) pode deixar em branco ou deletar do arquivo.
```

# 4 - Envie as alterações

Após criar o arquivo dentro de `pull-request/assinaturas` volte ao seu terminal de escolha e execute:

`git add *`

`git commit -m "sua mensagem de commit"`

`git push origin nome-da-sua-branch`

Ao commitar suas alterações em uma branch novinha em um repositório derivado de um Fork o GitHub irá automaticamente identificar que você esta tentando criar um pull request.

Basta voltar ao repositório _forkado_ em seu perfil para notar o seguinte botão:

<p align="center">
  <img src="https://raw.githubusercontent.com/aprenda-git/pull-request/define-tutorial-inicial/imagens/compare.png">
</p>

O mesmo te levará para uma página no repositório original (por isso o fork aponta o tempo todo para ele) onde você poderá criar de fato seu pull request.

# 5 - Crie seu pull request

Alguns repositórios fazem uso de templates para auxiliar as pessoas no processo de elaboração de uma boa mensagem de pull request. Não esqueça de marcar as caixinhas dizendo que segui os passos corretamente.

Clique em `Create pull request` e :tada: parabéns.

Seu pull request foi criado com sucesso. Em breve iremos revisar o conteúdo enviado para nos certificarmos de que o mesmo não contém nada ofensivo e iremos prosseguir com o processo de _merge_.
