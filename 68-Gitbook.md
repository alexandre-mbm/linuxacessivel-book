# Testando um livro gitbook localmente

Usando o serviço Gitbook integrado ao GitHub, a edição do livro não se dá pelo site [gitbook.com], e sim localmente. O conjunto de arquivos Markdown do livro está em repositório Git que é empurrado no GitHub. O repositório no GitHub tem um WebHook que avisa o sistema Gitbook quando acontece um _push_. Então o sistema Gitbook gera o livro com o novo estado dos arquivos, recuperando esses arquivos do GitHub que acabara de ser atualizado.

Concluimos que com a integração Gitbook-GitHub, a edição dos arquivos é toda local, certo?

Então torna-se-se muito conveniente termos uma forma de testar o livro localmente, antes de empurrar as alterações (commits) para o GitHub. Esse teste é realizado mediante uso do utilitário `gitbook-cli`.

## 1) Instalar o gitbook-cli

```console
$ npm install -g gitbook-cli
```
Para isso você precisa ter o [NodeJS] instalado previamente.

## 2) Executando o servidor de testes

A partir do diretório local de repositório Git, faça:

```console
$ gitbook serve
```

## 3) Finalmente, o teste

Então, agora, para testar o livro localmente, acesse http://localhost:4000

[gitbook.com]: http://gitbook.com
[NodeJS]: nodejs.md
