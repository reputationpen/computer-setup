*this only works on intel, but can prolly be modified for amd if you try harder*

# Downloads

start by copying both .bat files (BatteryStart and BatteryStop) to your C:/ drive
copy the ThrottleStop_9.6 folder to program files
copy the ThrottleStop.lnk to *%appdata%\Microsoft\Windows\Start Menu\Programs*
open task scheduler and import all 3 .xml's in the TaskScheduler folder
download both power plans in Power Plans folder and import them with admin cmd, `powercfg -import <path to power plan>`
install Intel Graphics Command Center from windows store

# The fun part

### 1. Throttlestop
open throttlestop and make sure it found the powerplans. you might have to reselect them in the drop down. High Performance for the performance profile and Please Don't Die for the battery profile.
make sure the undervolt is stable (FIVR page), if not bump up the offset voltage for cpu cache and cpu core until you stop blue-screening. make sure cpu cache and cpu core are the same.

### 2. Background Tasks
disable any unneeded startup tasks or background programs. if you want  something on startup but don't want it always running when on battery, add it to the .bat files from before following the syntax in them
check in task manager startup page, the startup folder *%appdata%\Microsoft\Windows\Start Menu\Programs\Startup*, and in Task Scheduler

### 3. Services
All non-Microsoft services should be disabled, unless you specifically need it
Type services in the windows search to open it
**Warning: DO NOT modify anything you are unsure of. This may render your computer unbootable.**
Go to the Services tab, then click "Hide all Microsoft Services"

### 4. Windows Appearance Settings 
Search "perfomance" in the windows search and uncheck:
- Animations in the taskbar
- Enable Peek
- Fade or slide menus into view
- Fade or slide ToolTips into view
- Fade out menu items after clicking
- Show shadows under mouse pointer
- Show shadows under windows
- Slide open combo boxes
- Use drop shadows for icon labels on the desktop

### 5. Drive Sleep
open regedit
go to *HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Power\PowerSettings\0012ee47-9041-4b5d-9b77-535fba8b1442\0b2d69d7-a2a1-449c-9680-f91c70521c60*
There should be a Description that says ‘Configures the LPM state’, as well as an ‘Attributes’ DWORD with the value 1. Change the value of ‘Attributes’ to "2”
Now go to windows search, type edit power plan > Change advanced Power Settings > Hard disk > ACHI Link power Management and set it to Lowest. If that is not an option, change it to HIPM+DIPM.

### 6. C States
open the C# section in throttlestop and check if the package C states are mostly in C7-C10. if they are, skip this section

It is somewhat unknown what exactly causes the issue, but it's usually a generic or outdated disk-related driver. 
- Try updating your disk drivers. 
- If you have a SATA based SSD, updating the ACHI controller may work
- Some have reported success by uninstalling Intel Rapid Storage Technology (IRST) or installing IRST and disabling a performance related setting. Some users have reported success by enabling IRST SATA power savings.
- it may also be any other driver, like Realtek Drivers for LAN/Ethernet or Wifi
- look for the driver download page for the laptop and try installing ones from there too
- Enabling DevSleep and DIPM appears to also work on some systems. On some systems, adding and removing devices (USBs, etc) change C state residency.
- if 'powercfg -energy' report says there are USB devices without selective suspend - you can force them to use it: 
    find 'SelectiveSuspendEnabled' under HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Enum\HID and HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Enum\USB\ subkeys, changing 0 to 1 (or 00 to 01) forces it on.
    After you forced Selective suspend, check Device Manager and enable "Windows can power down this device" for USB devices.

After a reboot, your package should idle at C6/C7/C8, depending on your manufacturer and CPU.

### 7. Intel Graphics 
make sure the latest drivers are installed, and turn on all the power saving features in Intel Graphics Command Center
