START WITH DOWNLOADING THIS REPOSITORY

# Bloat Removal

Go to https://github.com/builtbybel/ThisIsWin11/releases  
Download latest release  
Run ThisIsWin11  
Go to the Customize tab (second one) and click the plus in the top right, import adamsprofile.tiw1  
Fix Issues  
Go to the Apps tab (third one) and click the 3 dots in the top middle and import adamsbloat.txt  
Empty Bin  
Go the the Automate tab (fifth one) and run both srips in the Edge category  
Close the app and delete the files  
Restart computer  

# Chocolatey

### Install :

Open Powershell as Admin  
Run `Get-ExecutionPolicy`. If it returns Restricted, then run `Set-ExecutionPolicy AllSigned` or `Set-ExecutionPolicy Bypass -Scope Process`  
Then run `Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))`  


### Script (paste into terminal) :

`
choco install 7zip -y && choco install discord -y && choco install firefox -y && choco install teamviewer -y && choco install inkscape -y && choco install steam -y && choco install bitwarden -y && choco install geforce-experience -y && choco install vscode -y && choco install slack -y && choco install hot-chocolatey -y && choco install icue -y && choco install cpu-z -y && choco install obs-studio.install -y && choco install nodejs-lts -y && choco install bonjour -y && choco install openjdk -y && choco install twinkle-tray -y && choco install bitvise-ssh-client -y && choco install openjdk -y && choco install autohotkey -y && choco install blender -y && choco install firefoxpwa -y && choco install pdf24 -y
`


# Manual Downloads / Setup

**If on a laptop, go to laptopbattery.md**

### Firefox Style Setup :

Login to Firefox  
Login to Bitwarden  
Change settings for custom scrollbar extension  
Set Firefox to default browser

### Other Program Downloads :

adobe suite 	https://1drv.ms/u/s!AtZJZY-xh88UkS606M0fKUsPuC4g?e=rWuLMT  
solidworks	  https://solidworks.com/SEK  
grabcad	    	https://s3.amazonaws.com/desktop.grabcad.com/GrabCAD-Workbench-installer.exe  
nvidia broadcast    https://www.nvidia.com/en-us/geforce/broadcasting/broadcast-app/  
microsoft office    https://1drv.ms/u/s!AtZJZY-xh88UngLeMYcoutsJlho9?e=eIua1m
beeper    https://www.beeper.com/download
synergy 3    https://symless.com/synergy/download

Uninstall unneeded windows bloat  

Clean up taskbar and windows menu  

Download any games you want from steam, and you're done  
