# Markdown para escrever gitbooks

Estamos falando de uma linguagem que é usada para marcar formatação em arquivos de texto simples. No uso dela, a intenção não é que o nosso destinatário leia diretamente o conteúdo do `arquivo.md` em um editor de textos. Geralmente uma ferramenta, serviço ou conversor encarrega-se de converter Markdown em HTML e o resultado pode ser exibido (renderizado) como uma página web qualquer.

Entre outras grandes vantagens em manter seu conteúdo como "código fonte", texto simples, que é o que acontece quando usa-se Markdown, temos:

1. **Controle** ‒ arquivos de texto podem ser intuitivamente organizados e guardados
2. **Independência tecnológica** ‒ é possível usar conversores e obter resultados e formatos variados
3. **Simplicidade** ‒ a sintaxe Markdown está muito longe de ser complexa ou inútil!

## Características de um artigo

Nosso gitbook é basicamente uma reunião de artigos e tutoriais. Para uma apresentação elegante, precisamos usar negritos, itálicos, hiperligações, códigos em linha, blocos de código, cabeçalhos (até 6 níveis), listas não numeradas e listas numeradas. Eventualmente tabelas e notas de rodapé.

## Sintaxe

Nas subseções desta seção abordaremos como **escrever invisual** cada principal recurso de formatação que Markdown embute e nos interessa.

Existem outras formas de obter os mesmos resultados que são ensinados. Por uma questão de padronização e simplificação, aprenderemos formas únicas de marcar cada tipo de formatação que nos interesse.

### Negrito

Aplicável a: linha, expressão ou palavra. Não deve haver quebra de linha dentro de uma marcação de negrito.

Abre-se com `**` dois asteriscos colados ao conteúdo marcado. E fecha-se com `**` dois asteriscos colados ao conteúdo marcado.

#### Exemplos

- Palavra "casa" em negrito: `**casa**`
- Expressão "casa fechada" em negrito: `**casa fechada**`

### Itálico

Aplicável a: linha, expressão ou palavra. Não deve haver quebra de linha dentro de uma marcação de itálico.

Abre-se com `_` um _underscore_ colado ao conteúdo marcado. E fecha-se com `_` um _underscore_ colado ao conteúdo marcado.

#### Exemplos

- Palavra "casa" em itálico: `_casa_`
- Expressão "casa fechada" em itálico: `_casa fechada_`

### Hiperligação

Aplicável a: linha, expressão ou palavra. Não deve haver quebra de linha dentro de uma marcação de hiperligação.

A marcação de uma hiperligação tem duas partes. A primeira parte é a DESCRIÇÃO do alvo, e a segunda parte é o ALVO propriamente dito.

Além disso, existe a hiperligação marcada em linha e a hiperligação marcada por referência. A hiperligação marcada por referência é útil quando queremos deixar o código mais limpo, separando descrições e seus respectivos alvos. Estes ficam numa espécie de dicionário que é posicionado como bloco de linhas em linhas seguintes; abaixo de algum parágrafo ou lá no final do arquivo.

#### Hiperligação marcada em linha

É uma marcação do tipo: `[DESCRIÇÂO](ALVO)`

Onde:

- DESCRIÇÃO é linha inteira, expressão ou palavra de seu texto
- ALVO é nome de arquivo, URL ou apontamento de seção como `#id-do-título-html`

##### Exemplos

- Palavra "Google" linkando o Google: `[Google](http://www.google.com.br)`
- Expressão "Buscador Google" linkando o Google: `[Buscador Google](http://www.google.com.br)`
- Expressão "primeiro capítulo" linkando o arquivo `01-Alias.md`: `[primeiro capítulo](01-Alias.md)`

#### Hiperligação marcada por referência

Imagine que num determinado parágrafo de seu texto você quer colocar muitas hiperligações. Se usar hiperligação marcada em linha, do jeito que foi ensinado acima, o código Markdown do parágrafo ficará muito poluído. É nesses casos que é indicado usar hiperligação marcada por referência.

Esse tipo de marcação de hiperligação separa as descrições e seus respectivos alvos, que ficam numa espécie de dicionário à parte, bloco de linhas dentro do mesmo arquivo.

Não teremos uma subseção "Exemplos" para hiperligação marcada por referências. Segue um único exemplo que é auto-explicativo.

"Este parágrafo tem link para [Google](http://www.google.com.br), [Yahoo](http://yahoo.com), [GitHub](http://www.github.com), [Gitbook](http://gitbook.com) e [linuxacessível .org](http://linuxacessivel.org)"

Se fossem usadas hiperligações marcadas em linha, o código seria:

```markdown
"Este parágrafo tem link para [Google](http://www.google.com.br), [Yahoo](http://yahoo.com), [GitHub](http://www.github.com), [Gitbook](http://gitbook.com) e [linuxacessível .org](http://linuxacessivel.org)"
```

Mas fazendo com hiperligações marcadas por referência, podemos ter uma linha de código simplificada, seguida por um código de dicionário (para os alvos):

```markdown
"Este parágrafo tem link para [Google], [Yahoo], [GitHub], [Gitbook] e [linuxacessível .org]"

[Google]: http://www.google.com.br
[Yahoo]: http://yahoo.com
[GitHub]: http://www.github.com:
[Gitbook]: http://gitbook.com
[linuxacessível .org]: http://linuxacessivel.org
```

Note no código acima que o bloco de linhas agrupadas que constitui o dicionário de alvos precisa estar "separado", ou seja, após uma linha em branco. Na verdade, você pode optar por ter um grande e único dicionário, no final do arquivo. Porém, nem sempre essa será uma boa estratégia.

_Continua..._
