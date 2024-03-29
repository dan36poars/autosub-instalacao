# autosub-instalacão

## instalar o python

link: https://www.python.org/downloads/release/python-2712/

para computadores 64bits.
Windows x86-64 MSI installer

para computadores 32bits.
Windows x86 MSI installer

versão: 2.7.12 

criar a pasta c:\python27

siga as imagens para instalação

![passos para instalação](/img/py01.jpg "python instalação")
![passos para instalação](/img/py02.jpg "python instalação")<br>
a seta vermelha indica para instalar o caminho do python no path do sistema operacional.<br>
![passos para instalação](/img/py03.jpg "python instalação")
![passos para instalação](/img/py04.jpg "python instalação")

## Arquivos: 

copie para dentro da pasta c:\python27 os arquivos:

- ffmpeg.exe
- ffplay.exe
- ffprobe.exe

pode-se encontrar os arquivos no link:
https://ffmpeg.zeranoe.com/builds/

- testar na linha de comando do windows:

 `c:\python -V`

  `c:\ffmpeg`

imagens corretas das instalações respectivamente.

![passos para instalação](/img/cmd01.jpg "python instalação")

![passos para instalação](/img/cmd02.jpg "ffmpeg instalação")

## instalação autosub

Há varias maneiras para instalar o autosub. a mais simples
é pela linha de comando do windows

digite na linha de comando do prompt: ( o pip é um gerenciador de pacotes do python )

    C:\Python27\Scripts\pip.exe install autosub

![passos para instalação](/img/autosub-install-01.jpg "autosub instalação")

mostra a lista de suporte para detecção de idiomas

code
    
    c:\python c:\Python\scripts\autosub_app.py --list-languages

![passos para instalação](/img/autosub-install-02.jpg "autosub instalação")

dentro da pasta C:\Python27\Scripts o autosub estará sem a 
extensão py. baixe o arquivo autosub_app.py e mova-o para esta
pasta. algumas modificações foram feitas nesse arquivo. o diferenciando
do outro arquivo autosub sem extensão .py

reinicie o windows.

### gerar legendas


gerar legenda para idioma em inglês  acesse a pasta onde esta o arquivo de video no
qual quer gerar a legenda e o video deve ter o audio em inglês e abra o terminal de comando:

![passos para instalação](/img/autosub-install-03.jpg "autosub instalação")

    shift + botão direito do mouse na area em branco dentro da pasta
    ao surgir o menu selecione abrir janela de comando aqui.

no prompt de comando digite:

comando para gerar a legenda:

    C:\Python27\python.exe C:\Python27\scripts\autosub_app.py -S en -D en (nome_do_video).mp4

o que esta em parenteses é o nome do arquivo de video.

para exemplo, o video1.mp4, logo ficará.

    C:\Python27\python.exe C:\Python27\scripts\autosub_app.py -S en -D en video1.mp4

![passos para instalação](/img/autosub-install-03.jpg "autosub instalação")

ou

    python C:\Python27\scripts\autosub_app.py -S en -D en video1.mp4

![passos para instalação](/img/autosub-install-03.jpg "autosub instalação")
    

irá gerar um arquivo com extensão srt no mesmo local do arquivo que foi analizado.
Obviamente a transcrição pode conter algumas inconsistências.
Mas ajudará bastante na velocidade para transcrever arquivos
e legenda-los.


um abraço! e espero que este tutorial ajude.

fonte do material: https://github.com/agermanidis/autosub/issues/31
