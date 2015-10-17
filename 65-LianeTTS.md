# Instalar a voz Liane TTS no Orca

_Texto da mensagem de abertura do tópico "[{linuxacessivel.org} Instalando a voz Liane TTS no GNU/Linux (tutorial)][postagem]", no fórum do Projeto Linux acessível, postado em 17 de outubro de 2015 15:29, por **Lucas Antonio**. Publicado aqui após autorização._

---

[postagem]: https://groups.google.com/d/msg/linuxacessivel/UtQuXwKS6UQ/JqyLEHvtBgAJ

Prezados amigos, eis que depois de umas duas horas tentando instalar a voz Liane TTS no Orca, finalmente tive êxito.
O processo não é nada nada intuitivo, e contém várias armadilhas que facilmente emudecem o sistema.
Em vista disso, trago-vos um tutorial bastante detalhado com o qual, se desejarem, poderão fazer download e instalação da voz sem sustos nem erros.
Atenção! Os iniciantes não devem realizar tal procedimento, pois ele é um tanto quanto complexo para quem não tem um conhecimento básico do funcionamento geral do terminal, do speech-dispatcher e do orca.
A principal vantagem de usar a Liane no Orca, no meu entendimento, é a velocidade.
Enquanto o Espeak atinge 450WPM, a Liane atinge facilmente até 700WPM.
Notem que, em certa parte da instalação, necessitar-se-á da ajuda de um vidente, pois o speech-dispatcher deverá ser desativado.

Prontos? Vamos lá (funciona em sistemas Debian e derivados):

1 - Abra um terminal (ctrl+alt+t) e digitem os seguintes comandos, teclando enter após cada um deles.

sudo su

(sua senha)

wget http://intervox.nce.ufrj.br/~serpro/lianetts.tar.gz

tar -xzvf lianetts.tar.gz

cd liane_0.7

make

Aparecerão algumas instruções, ignorem-as com enter.
Se tudo está ocorrendo de forma apropriada, vocês ouvirão uma mensagem de boas vindas com a voz Liane TTS.

Agora vem a parte mais difícil, prestem atenção para não fazer bobagem!

Reiniciem o computador, e notem que ele não vai falar nada (isso é normal).
Com a ajuda de um vidente, abram o terminal (ctrl+alt+t), e escrevam os seguintes comandos, teclando enter após cada um deles:

sudo su

(sua senha)

killall orca

killall speech-dispatcher

gedit /etc/speech-dispatcher/speechd.conf

Agora, se tudo está ocorrendo como devido, abrirá um arquivo de configurações do speech-dispatcher através do gedit.
Selecione tudo com ctrl+a, e em seguida apague todo o texto com backspace.
Quando o arquivo estiver em branco, cole o seguinte (como segue):

# inicio das configuracoes

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

# fim das configuracoes

Pronto! Salve o arquivo com ctrl+s, feche o gedit, feche o terminal e reinicie o sistema (certificando-se de haver salvo o arquivo que acabamos de alterar).
Agora podemos dispensar a ajuda de um vidente, pois a partir daqui a voz deve falar.

Agora prestem atenção para os avisos finais, não esqueçam!
A configuração do Orca será reiniciada, e vocês terão de configurá-lo novamente.
Se ele não iniciar-se automaticamente, abram através do comando alt+f2 digitando "orca" sem aspas.
Quando forem alterar a velocidade da voz, não configurem para mais de 95%, pois se fizerem isso o sistema não vai funcionar.
A velocidade, quando em 96, 97, 98, 99 ou 100% fica muda, e só conseguimos ouvir uns clecks inconvenientes.

Com esse pequeno tutorial espero ter facilitado grandemente a instalação dessa voz no Orca, pois tive muita dificuldade para instalar sem instrução alguma.
Sugiro que os iniciantes no Linux não façam tal procedimento, pois poderão causar erros ou conflitos insolúveis. Por segurança, façam todos os backups que julgarem necessários.

Forte abraço, Lucas.