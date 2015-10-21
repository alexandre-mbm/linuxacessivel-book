# Testando um livro gitbook localmente

Usando o serviço Gitbook integrado ao GitHub, a edição do livro não se dá pelo site [gitbook.com], e sim localmente. O conjunto de arquivos Markdown do livro está em repositório Git que é empurrado no GitHub. O repositório no GitHub tem um Webhook que avisa o sistema Gitbook quando acontece um _push_. Então o sistema Gitbook gera o livro com o novo estado dos arquivos, recuperando esses arquivos do GitHub que acabara de ser atualizado.

Concluimos que com a integração Gitbook-GitHub, a edição dos arquivos é toda local, certo?

Então torna-se-se muito conveniente termos uma forma de testar o livro localmente, antes de empurrar as alterações (commits) para o GitHub. Esse teste é realizado mediante uso do utilitário `gitbook-cli`, um software que nos proporcionará instanciar um servidor de testes local para _build_ automático do livro.

1. [Instalando o gitbook-cli](#1-instalando-o-gitbook-cli)
2. [Executando o servidor de testes](#2-executando-o-servidor-de-testes)
3. [Finalmente, o teste](#3-finalmente-o-teste)
4. [Vantagens e desvantagens](#4-vantagens-e-desvantagens)

## 1) Instalando o gitbook-cli

```console
$ npm install -g gitbook-cli
```
Para isso você precisa ter o [NodeJS] instalado previamente.

## 2) Executando o servidor de testes

A partir do diretório local de repositório Git, faça:

```console
$ gitbook serve
```

Se o servidor está em execução, os resultados das edições salvas podem ser conhecidos renderizados HTML no navegador de Internet (Firefox). O _build_ do livro é refeito automaticamente quando qualquer arquivo markdown é salvo. Página de livro que estiver aberta no navegador será recarregada automaticamente, poucos segundos após o salvamento do arquivo (se não houve erros fatais).

## 3) Finalmente, o teste

Então, agora, para testar o livro localmente, acesse http://localhost:4000

Se você quer ir direto ao teste do arquivo nomeado `01-Alias.md`, pegue esse nome, troque a extensão `.md` pela extensão `.html`, e adicione-o à URL, assim: http://localhost:4000/01-Alias.html

## 4) Vantanges e desvantagens

Uma grande vantagem de usar `gitbook-cli` invés de simplesmente avaliar uma renderização HTML qualquer para seu arquivo markdown, é a integração com o `LIST.md` e o `SUMMARY.md`. Principalmente com este último, pois ele existe no padrão Gitbook, sendo responsável por gerar a lista sumário de navegação do livro.

Se seus arquivos markdown estão OK para o Gitbook, não estão com sintaxe quebrada, o _build_ do livro será feito e refeito com sucesso. Se seu `SUMMARY.md` tem todas as entradas de sumário que você quer que o livro possua, corretamente escritas como [hiperligações](64-Markdown.md#hiperligação) na lista não ordenada, você poderá [navegar o livro](#3-finalmente-o-teste) sem problemas — o livro terá habilitado, na lista de navegação e na busca, o item de sumário referente ao novo arquivo.

Uma pequeníssima desvantagem de usar o `gitbook-cli` para testar o livro é que você precisará manter num terminal aberto em separado o `gitbook serve` em execução. Em momentos oportunos, você deverá voltar a aquela tela e checar se a execução do servidor não fora interrompida por falha de _build_. Sob determinado aspecto, temos nesta "monitoração de _build_" mais vantagem do que desvantagem.

[gitbook.com]: http://gitbook.com
[NodeJS]: nodejs.md
