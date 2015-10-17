# Instalar a voz Liane TTS no Orca

_Texto da mensagem de abertura do tópico "[{linuxacessivel.org} Instalando a voz Liane TTS no GNU/Linux (tutorial)][postagem]", postada no fórum do projeto Linux Acessível em 17 de outubro de 2015 15:29, por Lucas Antonio. Publicamos aqui após autorização, sob licença [CC-BY 4.0]._

<!-- O texto pode vir a ser modificado por coautores, colaboradores do projeto linuxacessivel-book. Por enquanto foi mantido o aviso acima com a finalidade de preservar ao máximo a expressão original do autor. Ele escrevera em primeira pessoa dirgindo-se a um grupo virtual. -->

---

[postagem]: https://groups.google.com/d/msg/linuxacessivel/UtQuXwKS6UQ/JqyLEHvtBgAJ
[CC-BY 4.0]: https://creativecommons.org/licenses/by/4.0/deed.pt_BR

Prezados amigos, eis que depois de umas duas horas tentando instalar a voz Liane TTS no Orca, finalmente obtive êxito. O processo não é nada nada intuitivo, e contém várias armadilhas que facilmente emudecem o sistema.

Em vista disso, trago-vos um tutorial bastante detalhado com o qual, se desejarem, poderão fazer download e instalação da voz sem sustos nem erros.

**Atenção! Os iniciantes não devem tentar realizar tal procedimento**, pois ele é um tanto quanto complexo para quem ainda não tem suficiente conhecimento básico do funcionamento geral de um terminal, do speech-dispatcher e do leitor de telas Orca.

A principal vantagem de usar a Liane no Orca, no meu entendimento, é a velocidade. Enquanto o Espeak atinge 450 WPM, a Liane atinge facilmente até 700 WPM.

Em certa parte da instalação necessitar-se-á da ajuda de um vidente, pois o speech-dispatcher deverá ser desativado.

**Requisitos:** funciona em sistemas Debian e derivados.

## Você está pronto? Vamos lá!

Seguiremos algumas etapas:
1. [Baixar e compilar](#1-baixar-e-compilar)
2. [Configurar speech-dispatcher](#2-configurar-o-speech-dispatcher)
	1. [Preparando-se para lida com o sistema mudo](#i-preparando-se-para-lidar-com-o-sistema-mudo)
	2. [Editando o arquivo](#ii-editando-o-arquivo)
	3. [Vidente dispensado.](#iii-vidente-dispensado)
3. [Avisos finais muito importantes!](#3-avisos-finais-muito-importantes)

### 1 - Baixar e compilar

1. Abra um terminal combinando `Ctrl+Alt+T`, e digite os seguintes comandos teclando `ENTER` após cada um deles.
```
sudo su
	(sua senha)
wget http://intervox.nce.ufrj.br/~serpro/lianetts.tar.gz
tar -xzvf lianetts.tar.gz
cd liane_0.7
make
```
2. Aparecerão algumas instruções. Ignore-as com `ENTER`.

Se tudo está ocorrendo de forma apropriada, você ouvirá uma mensagem de boas vindas com a voz Liane TTS.

### 2 - Configurar o speech-dispatcher

Agora vem a parte mais difícil. Preste atenção para não fazer bobagem!

#### i) Preparando-se para lidar com o sistema mudo

1. Reinicie o computador. E note que **ao retornar ele não vai falar nada**. Isso é normal!
2. Com a ajuda de um vidente, abra o terminal pressionando `Ctrl+Alt+T` e passe os seguintes comandos teclando `ENTER` após cada um deles:
```
sudo su
	(sua senha)
killall orca
killall speech-dispatcher
gedit /etc/speech-dispatcher/speechd.conf
```

Agora, se tudo está ocorrendo como devido, abrir-se-á um arquivo de configurações do speech-dispatcher, no editor de textos Gedit.

#### ii) Editando o arquivo

1. Selecione tudo com `Ctrl+A` e em seguida apague todo o texto com `Backspace`.
2. Quando o arquivo estiver em branco, cole nele o seguinte conteúdo:

```aconf
# inicio das configurações

LogLevel  3

LogDir  "default"

DefaultVolume 100

DefaultVoiceType  "FEMALE1"

DefaultLanguage  "pt"

AddModule "lianetts"       "sd_generic"   "lianetts-generic.conf"
AddModule "espeak"       "sd_espeak"   "espeak.conf"

AddModule "dummy"         "sd_dummy"      ""

DefaultModule lianetts

LanguageDefaultModule "en"  "espeak"

Include "clients/*.conf"

# fim das configurações
```

**Pronto!** Salve o arquivo com `Ctrl+S`, feche o Gedit, feche o terminal, e reinicie o sistema. **Não esqueça de salvar!**

#### iii) Vidente dispensado.

A partir de agora podemos dispensar a ajuda do vidente. O sistema deverá estar falando!

A configuração do Orca será reiniciada, e você precisará configurá-lo novamente. Se ele não for iniciado automaticamente, abra-o pelo `Alt+F2`, digitando lá o comando `orca`.

### 3 - Avisos finais muito importantes!

Quando você for alterar a velocidade da voz, não configure para mais de **95%**, pois se fizer isso o sistema não funcionará. Ele fica praticamente MUDO quando a velocidade é configurada para 96, 97, 98, 99 ou 100%. Nessas condições nós somente conseguimos ouvir uns "clecks" inconvenientes.

## Ufa, terminou!

Com este pequeno tutorial eu espero ter facilitado enormemente, para vocês, a instalação da voz Liane TTS no Orca, pois tive muita dificuldade para instalá-la sem instrução alguma.

Sugiro que os iniciantes no GNU/Linux não tentem tal procedimento. Pode acontecer erros ou conflitos imprevistos e insolúveis. Por segurança, os que forem tentar, façam todos os backups que julgarem necessários.

Forte abraço, Lucas.