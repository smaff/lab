[![Version](https://img.shields.io/badge/FakeImageExploiter-1.3-orange.svg?maxAge=259200)]()
[![Stage](https://img.shields.io/badge/Release-Beta-orange.svg)]()
[![Build](https://img.shields.io/badge/Supported_OS-Linux-orange.svg)]()


![FakeImageExploiter v1.3](http://2.1m.yt/EASUSH9.png)


## FakeImageExploiter v1.3 - backdoor images.jpeg[.exe]
    CodeName: Metamorphosis
    Version release: v1.3 (Beta)
    Author: pedro ubuntu [ r00t-3xp10it ]
    Distros Supported : Linux Ubuntu, Kali, Mint, Parrot OS
    Suspicious-Shell-Activity (SSA) RedTeam develop @2017



## Legal Disclamer:
    The author does not hold any responsibility for the bad use of this tool,
    remember that attacking targets without prior consent is illegal and punished by law.

<br /><br />

## Description:
    This module takes one existing image.jpeg and one payload.exe (input by user) and
    builds a new payload (agent.jpeg.exe) that if executed it will trigger the download
    of the 2 previous files stored into apache2 webserver (image.jpeg + payload.exe).
    This module also changes the agent Icon to match one file.jpeg icon. Then uses
    'hide known file extensions' to hidde the .exe extension (final: agent.jpeg.exe) ..


 
## Exploitation:
    FakeImageExploiter stores all files in apache2 webroot, zips (.zip) the agent,
    starts apache2 and metasploit services(handler), and provides a URL to send to
    target (triggers agent.zip download). As soon as the victim runs our executable,
    our picture will be downloaded and opened in the default picture viewer, our
    malicious payload will be executed, and we will get a meterpreter session.

    But it also stores the agent (not ziped) into FakeImageExploiter/output folder
    if we wish to deliver agent.jpeg.exe using another diferent attack vector.

    'This tool also builds a cleaner.rc file to delete payloads left in target'
    HINT: migrate to another process before using cleaner to delete payload.exe
![FakeImageExploiter v1.3](http://3.1m.yt/4G9BUSH.png)

<br /><br />

## Payloads accepted (user input):
    payload.exe (default) | payload.ps1 | payload.txt | payload.bat [Metasploit]
    "Edit 'settings' file before runing tool to use other extensions"
![FakeImageExploiter v1.3](http://1.1m.yt/38x_l5i.png)


## Pictures accepted (user input):
    All pictures with .jpeg (default) | .jpg | .png  extensions (all sizes)
    "Edit 'settings' file before runing tool to use other extensions"
![FakeImageExploiter v1.3](http://2.1m.yt/BsH0WiO.png)

<br /><br />

## Dependencies/Limitations:
    xterm, zenity, apache2, mingw32[64], ResourceHacker(wine)
    'Auto-Installs ResourceHacker.exe under ../.wine/Program Files/.. directorys'

    WARNING: To change icon manually (resource hacker bypass) edit 'settings' file.
    WARNING: Only under windows systems the 2º extension will be hidden (so zip it) 
    WARNING: The agent.jpeg.exe requires the inputed files to be in apache2 (local lan hack)
    WARNING: The agent.jpeg.exe uses the powershell interpreter (does not work againts wine).
    WARNING: The ResourceHacker provided by this tool requires WINE to be set to windows 7
![FakeImageExploiter v1.3](http://2.1m.yt/1mmrwiZ.png)



## Download/Install/Config:
    1º - Download framework from github
         git clone https://github.com/r00t-3xp10it/FakeImageExploiter.git

    2º - Set files execution permitions
         cd FakeImageExploiter
         sudo chmod +x *.sh

    3º - Config FakeImageExploiter settings
         nano settings

    4º - Run main tool
         sudo ./FakeImageExploiter.sh


<br /><br />

## Framework Banner
![FakeImageExploiter v1.3](http://2.1m.yt/KvgWyAF.png)
## settings file
![FakeImageExploiter v1.3](http://3.1m.yt/aQOyj70.png)
## Agent(s) in windows systems
![FakeImageExploiter v1.3](http://2.1m.yt/fa0CN5K.jpg)

<br />

### Special thanks:
**@null byte** | **@Yoel_Macualo** | **@0xyg3n** (SSA team menber)

**Suspicious-Shell-Activity (SSA) RedTeam develop @2017**
