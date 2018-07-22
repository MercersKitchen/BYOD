# BYOD
Computer Setup: Program Information and Settings

Power Reminders
1. Power Adaptor
   - If Adaptor is faulty, voltage is most important
   - Example HP 6560b Adaptor Numbers: 19V, 4.74A
   - Voltage must be exact
   - Current cannot be less
2. Power settings (High Power for Installations and Updating Only)
   - Change to High Power (Hard Drive Never sleeps, turn monitor off in 1 minute)
   - Lid Button "Does Nothing" (able to close lid if needed)
   - Remember to change Power setting Back to Balanced Power

Download Installation and Executable File Checksums Reminders

For MD5: see Install+WinMD5.pdf
- Use Program, WinMD5.exe, notes below
- Use Windows CMD Commands, notes below
- Use Linux Command, notes below

For sha-256: notes below with MD5 Program

For Passwords or Accounts: use LastPass Program or Chrome Extension;
Also try KeePass

### Steps for Single Boot Windows 7 Installation ... Additional Details Below
1. Download ISO Files from Microsoft
2. Create USB Installation Key
. Install WINDOWS
. Update Drives (Especially All Internet Connection Drivers)
  - Note: Display driver can be an issues; also manually install additional issues as needed
. Windows Update (repeat as necessary)
  - Common Error: time settings
  - May need to delete Update Contents, see note below
. Ensure all BIOS Settings Correct
. Windows Settings and Tasks
. Install additional programs as needed (copy all .exe files to Downloads Folder first using USB)
  - See Program List .txt
.

Reminder: machine may need multiple restarts

CAUTION: Complete the Installation, then update the machine, then register WINDOWS with Product Key
- OPTION: register windows by phone, see folder for more details

---

## Additional Details

### Creating USB Installation Key
- Research these URLs
  - https://www.microsoft.com/en-us/download/windows-usb-dvd-download-tool
  - http://www.fit-pc.com/wiki/index.php/How_to_make_Windows_7_bootable_install_USB_stick
  - http://www.howtogeek.com/191054/how-to-create-bootable-usb-drives-and-sd-cards-for-every-operating-system/
- Use Rufus as option to create Bootable USB for Windows Installation
  - Use USB Rufus Key

---

### Using the Rufus USB Key
- Start WINDOWS as normal on the Machine
- Open Key / Double Click Setup

---

### Driver Information and Installation
NOTE: Internet Connection Drivers are crucial and must be installed separately
- Windows Update is safest (and easiest) way to update and install additional drivers
Finding information about Drivers
- Use Windows Device Manager (Windows 7: Control Panel / Hardware and Sound / Devices and Printers)
- Device Manager / Properties for Component / Details / Hardware IDs
- Alternative
  - RightClick on ICON with !
  - See Troubleshoot, Google Full Driver Name
-

Important URLs used to Research Information
- https://www.pcilookup.com
  - Details to Use: VEN is vendor, DEV is Developer
  - Details found in Driver Error Menu or Windows Device Manager (Use Search to Locate folder)
  - Example Search: https://www.pcilookup.com/?ven=8086&dev=1503&action=submit
  - Ethernet Controller Driver Missing: VEN 8086, DEV 1503
  - PCI Lookup will return "82579V Gigabit Network Connection"
  - Google the description of device, include driver download
  - Returns: https://downloadcenter.intel.com/download/18713/Intel-Network-Adapter-Driver-for-Windows-7-?product=52963
  - Copy Driver to "Downloads Folder" of machine
  - Double Click to install (may need restart)

---

### BIOS Settings
- Check Memory and System with Tools
- Change Clock Settings, if necessary
- If Hard Drive can only be used in this one machine, enable Automatic Drive Lock function that uses BIOS password
  - Otherwise do not enable any drive locks
- Boot Options: not SD or Floppy (some "camera" .exe viruses and no floppies are used)
- Enable VT-X, Virtual Technology, in BIOS
- Administrator Settings?
- Enable audio alerts during boot
- Enable NumPad
- Turn off Volume for machine, if possible
- SATA Should be AHCI (IDE is for Windows XP and older)
- SATA Speed should be 6.0

- Change Region and Language
- Computer Name in System Properties
- Change Device Installation Settings for Drivers, to recommended

---

### Clock settings
- Control Panel / Date and Time / Internet Clock / Update Now
- Ensure Clock Setting is correct
- Troubleshoot: synchronize Internet Clock to System Tray Clock

---

### Deleting Windows Update Contents
- "Stop the Services first, then delete, then restart services"
- GUI Version: C Drive / Windows / Softwaredistribution
  - Use this to visually verify CMD Commands Successful
- CMD Version: stop the Windows Update Services
```
net stop bits
net stop wuauserv
```
- In GUI, actually delete the contents of the folder
- CMD: restart Windows update services
```
net start buts
net start wuauserv
```
- ReRun Windows Update

---

### Windows Settings and Tasks, additional items
- WINDOWS Defender: change settings in Options, Update and Scan
- Deal with all messages (firewall, security, backup, etc.)
- Folder Options
  - Enable Extensions (i.e .exe, for RansomWare Security)
  - ClickOff "Hide all Hidden Folders" (Want to see these)

---

# Program List
Notes for BYOD Student Machines and Computers that act like BYOD

Use these downloads to create a USB Key or a Folder of Executables and notes

**NOTE** : Create links in Start Menu and leave Desktop Clean

**CAUTION**: Never update programs without a plan
- Programs must work well together, make notes about what you download and when
- A new program or updated file might cause errors

---

## Paid Programs

### Snag It from TechSmith

---

## For Computers using SchoolZone (all) or PowerTeacher

### Ensure JDK matches PowerTeacher Java Version
- Currently 8u121, 20180613
- See PowerTeacher (PowerSchool / Progress Module / Click Here to install)
- Ensure Environmental Variable (Pathway) is set properly
  - CAUTION: no direct error message if typed with error

---

## Install Instructions for specific programs *or* computers not using EPSB Imaging services

### Chrome: ChromeSetup.exe, 20180613
- Install Flash, set to ask (esp. for Cisco Academy)
- Add LastPass Extension
- Test by Surfing

### Packet Tracer for Cisco Academy: Packet Tracer 7.1.1 for Windows 64 bit.exe, 20180613
- NOTE: will work on Windows 10
- Testing Packet Tracer: must login twice (first time for initial setup, second for testing)
  - Use PKA 2.2.3.4
  - Follow additional prompts
- Add Cisco Packet Tracer 7.1 FAQs.pdf
  - Add to My Documents / Cisco

###Video Player: vlc-3.0.3-win64.exe, 20180613
- Using VLC: https://lifehacker.com/the-best-hidden-features-of-vlc-1654434241

### PuTTY: putty-64bit-0.70-installer.msi, 20180623

### PuttyGen: puttygen.exe, 20180623

### TightVNC: tightvnc-2.8.11-gpl-setup-32bit.msi, 20180623
- https://www.tightvnc.com/download.php
- CAUTION: install Viewer and Server in specific applications
- Will Cause Security Issue

### Virtual Machine: VMware-player-12.5.9-7535481.exe, 20180623
- www.vmware.com

### Wire Shark: Wireshark-win64-2.6.1.exe, 20180614
- https://www.wireshark.org/#download
- Install USB Package
- Other packages are available, install these if you want to test them

### MD5 Checksum File Integrity
- Program: WinMD5.exe, 20180614
  - No Installation program, is executable
  - See Readme.txt and License for instructions
  - Drag and Drop usage
  - http://winmd5.com/
- WINDOWS CMD MD5 Checking
  ```
  certutil -hashfile FILENAME  MD5
  ```
- Linux MD5 Checking
  ```
  md5sum FILENAME
  ```
- sha-256 Windows: certutil -hashfile FILENAME  sha256
- sha-256 Linux: sha256sum FILENAME

### SD Card Programs, 20180614
- See Raspberry Pi Website for updated programs, new programs, etc.
- SD_CardFormatter0500SetupEN.exe
  - https://www.sdcard.org/downloads/formatter_4/
- win32diskimager-1.0.0-install.exe
  - https://sourceforge.net/projects/win32diskimager/files/latest/download
- Recuva: rcsetup153.exe
  - https://www.ccleaner.com/recuva
- Additional SD Recovery, not tested yet: DiskDigger, Version 1.18.17.2417, https://diskdigger.org/

### WYSIWYG (What You See is What You Get) Text Editors
- Test these with Hello World Program in Chrome, see index.html
- Notepad++: npp.7.5.6.Installer.x64.exe, https://notepad-plus-plus.org/ ,20180614
- Atom: AtomSetup-x64.exe, Version 1.27.2, 20180614

Installing and Personalizing Atom (Optional Settings and Additions)
- Why Atom: open multiple projects in one window
- See the Flight Manual: http://flight-manual.atom.io/
  - Set-up Section is good, use this with Video 1 below
  - Note: Tree View has parent, child, and sub notes
- Video #1: https://www.youtube.com/watch?v=U5POoGSrtGg
  - See the Rest of this Channel to get some ideas for using Atom
- Note about Signing in to GitHub through Atom
  - Must review permissions on a regular basis
  - For further ideas see: https://help.github.com/articles/authorizing-oauth-apps/

Suggestions for packages
- Already installed is Built In Plug-In for Spelling
  - adds suggestions for variables found in coding, nice feature
-

Additional Packages and themes for Atom: https://atom.io/packages

### 7 Zip: 7z1805-x64.exe, www.7-zip.com, 20180614

### GitHub Desktop: GitHubDesktopSetup.exe, 20180614

---

### Other Browsers for Testing CSS files

See Last Pass for up dated List
https://lastpass.com/misc_download2.php

Chrome: see above
Firefox: Firefox Installer.exe, https://www.mozilla.org/en-US/firefox/new/, 20140613
Opera: OperaSetup.exe, https://www.opera.com/, 20180613
  - Might be unsupported after 201808
Unknown: mx5.2.3.2000.exe, 20180614
Internet Explorer: installed with Windows

---

Additional Program Website List
- www.ubuntu.com
- www.canonical.com: for Ubuntu software updates
- SlackSetup.exe for messaging and Social Networking

Search Engines: Google's V8, Bing (for research and to find updates)

---

## Installation Instructions for a WAMP Server
See Folder and Notes from Installation

---
# Previous Versions Notes Not Deleted Yet

### TCPIP Stack Reset, Windows 7
```
Click Start / CMD Run as Administrator
ipconfig /flushdna
nbtstat -R
nbtstat -RR
netsh int reset all
netsh int ip reset
netsh winsock reset
```

---

### GitHub Classroom
- Must install Atom (AtomSetup-x64.exe) First (or Notepad++, etc.)
- Install Git-2.16.2-64-bit.exe (enable Atom or WYSIWYG choice)
- Install GitHub Desktop
