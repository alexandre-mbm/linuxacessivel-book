# `alias` ‒ Criando apelidos para comandos do Shell

_Atenção! O que é ensinado a seguir precisa ser adaptado para acessibilidade. Por enquanto está página somente existe para experimentação de navegação do serviço Gitbook_

O comando `alias` possibilita que se crie um apelido para determinado comando. Isso pode ser usado para lidar com um nome de comando totalmente diferente do original, por questões de costume. Por exemplo:

```sh
alias dir=ls
```

A criação de apelido acima faz com que comandar `dir` e comandar `ls` sejam exatamente a mesma coisa. A expressão `dir` passa a ser um apelido para o comando `ls`.

Um apelido também pode ser usado para simplificar um comando que você sempre passa com opções. Por exemplo, se você gosta de listar arquivos e diretórios em coluna única:

```sh
alias ls=ls -1
```

Agora, `ls` sendo apelido para `ls -1`, é dispensável digitar a opção `-1`. Em compensação, seu `ls` será sempre uma listagem de única coluna, obrigatoriamente, porque o apelido acaba por substituir o original.
