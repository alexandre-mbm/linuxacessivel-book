# NodeJS

É um [framework] para desenvolvimento de aplicações em Javascript.

Os programas feitos com NodeJS comumente são distribuídos e podem ser instalados por meio do Gerenciador de Pacotes do NodeJS, que é mais conhecido como [`npm`](npm). 

## Instalar em Arch Linux

```console
$ sudo pacman -S nodejs
```

## npm

Para instalar o pacote de NodeJS de um PROGRAMA, valendo para todo o sistema, fazemos:

```console
$ sudo npm install -g PROGRAMA
```

Nesse caso é muito importante usar a opção `-g`. Senão o NodeJS instalará tudo, toda uma árvore de pacotes (com dependências), no diretório atual.

É normal a execução de comandos do tipo `npm install` ser demorada. Especialmente se acontece para instalação em diretório atual limpo, localmente, sem a opçãom `-g`. Pois antes dos downloads e das instalações propriamente ditas, o comando calcula todas as dependências.

[framework]: http://pt.wikipedia.org/wiki/Framework
