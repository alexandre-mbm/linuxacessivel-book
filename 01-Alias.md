# `alias` ‒ Criando apelidos para comandos do Shell

_Atenção! O que é ensinado a seguir talvez precise ser adaptado para ensinar acessibilidade. Por enquanto esta página somente existe para experimentação da navegação em gitbooks._

---

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

## Salvar os apelidos de forma permanente

Os apelidos criados através do comando `alias` são perdidos quando você fecha a sessão de terminal, ou quando você reinicia a máquina.

Para que você não tenha de criar novamente esses apelidos toda vez que for usar o terminal, você pode inserir a criação dos apelidos dentro do arquivo de configurações `.bashrc`. Esse arquivo nada mais é do que um _shell script_ que é executado toda vez que uma sessão de terminal é iniciada.

### Passo-a-passo

1. Abra o arquivo `~/.bashrc` usando qualquer editor de textos;
2. No final do arquivo, insira as linhas de comando como se você estivesse digitando no terminal;
3. Salve e pronto! Nunca mais você vai perder seus apelidos.

Esteja atento a um dtalhe importante:

Após salvar esse arquivo de configuração, você precisa fazer o sistema recarregá-lo, para que os apelidos realmente fiquem disponíveis. Há duas maneiras de fazer isso:

**a)** Fechar a sessão corrente (ou o terminal) e abrir outro terminal  
**b)** Executar `source ~/.bashrc` na sessão corrente e continuar a usá-la