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
choco install 7zip -y && choco install discord -y && choco install firefox -y && choco install teamviewer -y && choco install synergy -y && choco install inkscape -y && choco install steam -y && choco install bitwarden -y && choco install geforce-experience -y && choco install vlc -y && choco install vscode -y && choco install slack -y && choco install chocolateygui -y && choco install icue -y && choco install cpu-z -y && choco install obs-studio.install -y && choco install nodejs-lts -y && choco install bonjour -y && choco install openjdk -y && choco install twinkle-tray && choco install bitvise-ssh-client
`


# Manual Downloads / Setup

~### Firefox Style Setup :~

~Login to Firefox  
Login to Bitwarden  
Change settings for custom scrollbar extension  
Set Firefox to default browser  
Download chrome.zip  
Download tst config  
Open firefox and go to about:config  
Set `toolkit.legacyUserProfileCustomizations.stylesheets` to true  
Go to about:support and click open profile folder  
Unzip chrome.zip into the profile folder  
Restart firefox  
Go to settings for tst and import the config file~  

### Airmessage Setup :

Download airmessage.ico  
Open cmd and run:  
`
npm install -g nativefier && nativefier "https://web.airmessage.org"
`  
Open `C:\Users\[User]\` and move the Airmessage install directory to `C:\Program Files\[Airmessage Install]`  
Create a shortcut for the exe  
Place airmessage.ico in the install directory  
Change the shortcut icon to airmessage.ico and rename it to Airmessage  
Move the shortcut to `C:\ProgramData\Microsoft\Windows\Start Menu\Programs`  


### Other Program Downloads :

adobe suite 	https://1drv.ms/u/s!AtZJZY-xh88UkS606M0fKUsPuC4g?e=rWuLMT  
solidworks	  https://solidworks.com/SEK  
grabcad	    	https://workbench.grabcad.com/workbench/download  
nvidia broadcast    https://www.nvidia.com/en-us/geforce/broadcasting/broadcast-app/  

Uninstall unneeded windows bloat  

Clean up taskbar and windows menu  

Download any games you want from steam, and you're done  
