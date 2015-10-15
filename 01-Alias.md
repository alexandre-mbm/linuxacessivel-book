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

# `alias` ‒ Salvando apelidos de forma permanente

Os apelidos criados através do comando `alias` São perdidos quando você fecha asessão no terminal ou quando você reinicia a sua máquina.
Para que você não tenha de criar novamente esses apelidos toda vez que uma sessão do terminal for aberta, você pode inserir a criação dos apelidos dentro do arquivo .bashrc.
Esse arquivo nada mais é do que um shell script que é executado toda vez que uma sessão no terminal é aberta.
Abra esse arquivo usando qualquer editor de textos e no final dele insira as linhas como se você estivesse digitando no terminal. Salve e pronto, nunca mais você vai perder os seus apelidos.
Após salvar esse arquivo você precisa executa-lo para que os apelidos sejam criados, o que pode ser feito de duas maneiras:
- **Feche a sessão corrente e abra novamente.
- **Execute o seguinte comando no terminal: ```
source .bashrc
```
