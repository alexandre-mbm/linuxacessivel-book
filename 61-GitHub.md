# Tornando-se usuário do GitHub

Este breve manual de usuário invisual para GitHub pressupõe conhecimento básico de Git e prática em navegação estrutual HTML.

Em caso de dúvidas, por favor escreva a [Alexandre Magno](mailto:alexandre.mbm@gmail.com). Ele buscará responder a você por e-mail particular e possivelmente corrigirá ou aperfeiçoará o manual.

Infelizmente a interface do GitHub é toda em inglês. Sendo assim, preste atenção nas leituras em inglês que são exemplificadas em cada instrução.

## Criando a conta

Na primeira tela nós vamos submeter informação que nos identifica.

1. **Acesse [github.com]**
1. O cursor (modo de foco) estará no primeiro campo que nos interessa — "_Pick a username_", que significa: **"Digite um nome de usuário"**.
1. Preencha a informação. Para os videntes, já neste momento, ao digitar, o sistema sinaliza quando um nome de usuário está reservado, em uso por outra pessoa. Não se preocupe com isso. Vamos tentar prosseguir e tentar finalizar o cadastro. Se algo der errado, voltaremos a este passo.
1. Pressione `TAB` e o cursor irá para o segundo campo de entrada que nos interessa — "_Your e-mail_", que quer significar: **"Digite seu endereço de e-mail"**.
1. Preencha a informação. Mais uma vez trata-se de um campo de identificação, você não poderá usar um endereço de e-mail que já tenha usado para cadastrar outro nome de usuário. Obviamente, você não pode e não deve tentar usar um endereço de e-mail de outra pessoa. O sistema de cadastramento lhe enviará e-mail de confirmação, ao final do processo.
1. Pressione `TAB`  e o cursor irá para terceiro campo de entrada que nos interessa — "_Create a password_", que quer significar: **"Digite uma senha para sua nova conta GitHub"**
1. Preencha a informação. Use pelo menos uma letra maiúscula e um numeral. A senha deve ter no mínimo 7 caracteres.
1. Pressione `TAB` e o cursor repousará em cima do botão de apertar "_Sign up for GitHub_". Em português, algo como: **"Cadastrar-se no GitHub"**.
1. Aperte o botão pressionando a tecla `ENTER`.

Se tudo aconteceu como o esperado e não houve erros no preenchimento do formulário, você será levado à segunda tela, para escolha do plano.

1. Pressione `t`para navegar até a tabela de planos de assinatura, uma tabela com 6 linhas e 4 colunas. Não se preocupe, o serviço tem um plano gratuito, e é o que vamos escolher.
1. **O plano padrão é gratuito!** Por segurança, seria interessante navegar a tabela, conhecendo as opções, e garantir nossa opção por ele. Infezlimente parece que a escolha por outro plano está inacessível. Vamos então pelos menos confirmar se o plano gratuito é o que está selecionado. Tecle `SETA-PARA-BAIXO` sucessivamente, até chegar à linha 6. O leitor de tela deverá ler: "_Free_ ponto _$0/month_ ponto _0_ ponto _Choosen_ botão de apertar". Atenção à última palava; deve ser "_Choosen_" (que singifica "Escolhido"), com "_n_" no final, e não "_Choose_" (que significa "Escolher"), sem o "_n_".
1. Pressione `TAB` e o cursor irá para uma caixa de seleção não selecionada: "_Help me set up an organization next_". Matenha desmarcado. Não nos interessa criar ou configurar uma organização agora. Queremos apenas criar um usuário comum, individual.
1. Pressione `TAB` e o cursor irá para o link "_[Learn more about organizations](https://help.github.com/categories/2/articles)_" (em português: "Aprender mais sobre organizações"). Não o acesse! Além dele ser em inglês, nesse momento não nos interessa saber sobre organizações de GitHub.
1. Pressione `TAB` mais um vez em finalmente você estará no botão de apertar "_Finish sign up_" para "**Finalizar o cadastro**". Pressione `ENTER`.
1. Um tela de início ou de "boas vindas", em inglês, será exibidas no endereço [github.com].

Um e-mail de confirmação de cadastro será enviado a você. Na verdade, o sistema do GitHub enviará dois ou três e-mails:

- **"_[GitHub] Please verify your email address_"** é o assunto do primeiro e-mail, que é o de confirmação de cadastro propriamente dito. A mensagem HTML tem um botão "_Verify email address_". Você deve clicá-lo para confirmar o cadastro confirmando (fazendo a verificação para) esse endereço de e-mail.
- **"_ambdm + GitHub = <3_"** é o assunto do segundo e-mail, uma mensagem de "boas vindas" dadas pela equipe que faz o GitHub.
- **_[GitHub] Attention: Your email address needs to be verified._"** foi um terceiro e-mail de confirmação que eu recebi, provavelmente por tentar acessar  [github.com] sem antes confirmar (fazer a verificação para) o endereço de e-mail a partir da primeira mensagem recebida.

Se algo der errado e o link de confirmação de endereço de e-mail estiver expirado ou inválido, você será levado a [github.com/settings/emails](https://github.com/settings/emails). Despreze isso e volte a sua Caixa de Entrada, pois você pode ter recebido uma terceira mensagem (como eu recebi; ver acima).

Uma coisa interessante a se notar é que o primeiro parágrafo (tecle `p` para chegar até ele) desta página é exatamente o seguinte:

> _Your **primary GitHub email address** will be used for account-related notifications (e.g. account changes and billing receipts) as well as any web-based GitHub operations (e.g. edits and merges)._

Ele nos explica, em inglês, que o endereço de e-mail principal de uma conta GitHub recebe notificações de mudanças na conta, cobranças (no caso dos planos pagos), e notificações de atividades em repositórios monitorados (mesclagens, _pull requests_, respostas a comentários, etc.).

Quando você conseguir confirmar seu endereço de e-mail por clique em link de confirmação recebido por e-mail, você será redirecionado a [github.com].

Lembre-se de que, no Firefox, `F6` nos permite alterar entre a barra de endereços e corpor da página.

<!-- TODO: seção "## Login" -->

## Acessando o próprio perfil

Todo perfil de usuário pode ser acessado por meio de uma URL na forma `github.com/NOMEDEUSUARIO`. Mas, para dificultar um pouco e termos a oportunidade de ir aprendendo navegação estrutural invisual de GitHub, vamos ao seu próprio perfil navegando os menus do site. Pressuposto que você já está logado.

1. **Acesse [github.com]**
1. Pressione `TAB` uma vez, para pular para o conteúdo da página — "_Skip to content_".
1. Pressione `L` duas vezes, para ir à segunda lista. A primeira lista começa com o link "_Pull requests_". A segunda lista, com um link que é alguma coisa sobre "_notifications_" (notificações). Essas listas são menus superiores horizontais.
1. Pressione `TAB` sucessivamente para ir ao terceiro item da lista (menu). Será o link "_View profile and more_" — em português: **"visualizar perfil e mais"**.
1. Pressione `ENTER` e abrir-se-á um submenu vertical flutuante.
1. Use `SETA-PARA-BAIXO` sucessivamente até encontrar o link "_Your profile_", que dá acesso ao **seu perfil**.
1. Clique o link com `ENTER` e a página de seu perfil será aberta.

## Conhecendo um perfil de usuário

- **Nome do usuário**
	- Se você quer rever o nome de usuário do perfil que está aberto, simplesmente tecle `1`, pois o nome será o único cabeçalho de nível 1 nesta página de perfil.
- **Cidade, e-mail e data de inscrição**
	- Estando no ponto inicial da página, tecle `L` três vezes para ir até a terceira lilsta. Navega-a com as setas verticais e conheça o local da pessoa (se ela declarou), o endereço de e-mail dela (se ela declarou), ou pelo menos a data em que esse usuário cadastrou-se no GItHub.
		- A informação da data estará em inglês. Algo como "_Joined on 21 Jun 2015_", que significa: "Entrou em 21 de junho de 2015"
- **Seguidores, projetos favoritos e pessoas seguidas**
	- Todo usuário de GitHub pode seguir outros usuários, favoritar projetos (marcado-os com estrelas), e ser seguido por outros.
		- A finalidade de favoritar projetos é apenas ter e compartihar com todos uma lista de projetos que por algum motivo um dia lhe interessaram.
		- Pessoas seguem umas às outras para dizer a todos que ambas tem afinidades nessa rede social que é o GitHub, de compartilhamento de projetos de código aberto. E também para serem notificadas (até por e-mail) de algumas das ações de quem elas seguem.
    - O perfil do usuário mostra um contador de seguidores, um contador de favoritos, e um contador de pessoas seguidas; nessa ordem. Para acessar esses contadores, percorra toda a lista anterior, aquela que teria cidade, e-mail e data de inscrição, e prossiga apertando `TAB` após a data. Serão 3 links para 3 respectivas páginas de listagem. Cada um está associado a um contador. Nos exemplos de leitura a seguir, um \* (asterisco) representa o número do contador. No real, as expressões estão em inglês e sem as áspas.
        - O primeiro link é o contador de seguidores
            - Leitura: "\* _Followers_ link ponto \* link"
        - O segundo link é o contador de projetos favoritos
            - Leitura: "\* _Starred_ link ponto \* link"
        - O terceiro link é o contador de usuários seguidos por este usuário que você está conhecendo
            - Leitura: "\* _Following_ link ponto \* link"
- **Para seguir ou não seguir um usuário...**
    1. Chegue aos contadores como ensinado acima e ultrapasse-os com mais um `TAB`
    2. Você estará em cima do botão de apertar que ou chama-se "_Follow_" (seguir) ou chama-se "_Unfollow_" (deixar de seguir). Basta apertar `ENTER` para alternar esse valor e com isso seguir ou deixar de seguir o usuário em questão.
- **Você quer bloquear este usuário? Ou denunciá-lo?**
	1. Apenas pressione `TAB` mais uma vez e você estará noutro botão de apertar. Este é um menu. Pressione `ENTER`
	2. Pressione `TAB` uma vez para chegar ao item de menu para bloquear ou desbloquear o usuário. Se o texto desse botão estiver sendo "_Block user_", apertá-lo com `ENTER` bloqueará o usuário. Se o texto desse botão estiver sendo "_Unblock user_", apertá-lo desbloqueará o usuário. A ação recarrega a página.
	3. Ou...
	Se você pressionou `TAB` duas vezes dentro do menu, estará em cima do botão de apertar "_Report abuse_", que serve para denunciar o usuário ao pessoal do GitHub. Por razões óbvias, não foi possível testarmos esse botão. Descubra sozinho como é a ação dele ou [envie a Alexandre Magno um e-mail candidatando-se a ser o usuário cobaia a ser denunciado durante um teste](mailto:alexandre.mbm@gmail.com).

<!-- TODO: melhor estratégia para contadores, a partir de cabeçalho nível 1 -->

<!-- TODO: estrutura a seção com subníveis -->

### Navegar a lista de repositórios de um usuário

Após passar os contadores<!-- TODO: linkar quando passar a existir (acima) --> pressionando `TAB` três vezes, passar o botão de seguir<!-- TODO: linkar quando passar a existir (acima) --> pressionando `TAB` uma vez, passar o menu de bloqueio ou denúcia<!-- TODO: linkar quando passar a existir (acima) --> pressionando `TAB` mais uma vez, e finalmente a aba de página "_Contributions_" (contribuições), a qual simplesmente está na ordem, prossiga com mais um`TAB` até a aba de página "_Repositories_" (repositórios). Então pressione `ENTER` e essa aba de página será aberta.

Na aba de página que você acabou de abrir, nomes de projetos/repositórios estarão como cabeçalhos de nível 3 que também são links. Após cada um deles haverá descrição do projeto (quando configurado pelo dono) e data de criação do projeto abreviada em inglês, ambos como parágrafos que podem ser visitados com a tecla `p`.

### Buscar repositórios de um usuário

Estando com a aba de página "_Repositories_" (repositórios) aberta, o campo de busca por repositórios no perfil sendo visitado é o segundo campo de formulário encontrado na página. Quando o conteúdo da página começa a ser explorado por `TAB`, esses campos de digitação tem prioridade. A passagem por eles é no modo de foco. Sendo assim, comece ou recomece a navegação da página, pressione `TAB` duas vezes, e você estará no campo de busca. Então é só digitar sua chave de busca e apertar `ENTER`. Você será levado à página de busca<!-- TODO: explicar a página de busca em nova seção --> com a listagem dos resultados.

<!-- TODO: assinatura de feed de atividades do usuário -->

<!-- pull requests e issues do meu usuário -->

[github.com]: http://github.com