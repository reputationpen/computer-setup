# Chocolatey

### Install :

Open Powershell as Admin  
Run `Get-ExecutionPolicy.` If it returns Restricted, then run `Set-ExecutionPolicy AllSigned` or `Set-ExecutionPolicy Bypass -Scope Process`  
Then run `Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))`  


### Script (paste into terminal) :

`
choco install 7zip -y && choco install discord -y && choco install firefox -y && choco install teamviewer9 -y && choco install synergy -y && choco install inkscape -y && choco install steam-client -y && choco install bitwarden -y && choco install geforce-experience -y && choco install vlc -y && choco install zoom -y && choco install vscode -y && choco install spotify -y && choco install slack -y && choco install chocolateygui -y && choco install intel-dsa -y && choco install everything -y && choco install figma -y && choco install icue -y && choco install cpu-z -y && choco install minecraft-launcher -y && choco install obs-studio -y
`


# Manual Downloads / Setup

### Firefox Style Setup :

Download chrome.zip  
Download tst config  
Open firefox and go to about:config  
Set toolkit.legacyUserProfileCustomizations.stylesheets to true  
Go to about:support and click open profile folder  
Unzip chrome.zip into the profile folder  
Restart firefox  
Go to settings for tst and import the config file  

### Airmessage Setup :

Download airmessage.ico  
Open cmd and run:  
`
npm install -g nativefier && nativefier "https://web.airmessage.org" "C:\Program Files\"  
`
Open C:\Program Files\[Airmessage Install]  
Create a shortcut for the exe  
Place airmessage.ico in the install directory  
Change the shortcut icon to airmessage.ico and rename it to Airmessage  
Move the shortcut to C:\ProgramData\Microsoft\Windows\Start Menu\Program  


### Other Program Downloads :

adobe suite 	https://1drv.ms/u/s!AtZJZY-xh88UkS606M0fKUsPuC4g?e=rWuLMT  
solidworks	  https://solidworks.com/SEK  
grabcad	    	https://workbench.grabcad.com/workbench/download  

Download any games you want from steam, and you're done
