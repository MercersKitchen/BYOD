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
3. Pre OS Installation Task List
   - Search for WiFi, LAN, Internet Drivers (or have alternate computer to search after installation)
   - Check BIOS to ensure USB is in Bootable Sequence
   - Find USB-1 if possible, might be a guess and check during initial installation


Download Installation and Executable File Checksums Reminders

For MD5: see Install+WinMD5.pdf
- Use Program, WinMD5.exe, notes below
- Use Windows CMD Commands, notes below
- Use Linux Command, notes below

For sha-256: notes below with MD5 Program
- Also able to ShiftRightClick on Folder, CRC SHA

For Passwords or Accounts: use LastPass Program or Chrome Extension;
Also try KeePass

### Steps for Single Boot Windows 7 Installation ... Additional Details Below
1. Download ISO Files from Microsoft
2. Create USB Installation Key
3. Install WINDOWS
   - Note: click off WIN Tool Addition
4. Update Drives (Especially All Internet Connection Drivers)
   - Note: Display driver can be an issues; also manually install additional issues as needed
5. Ensure all BIOS Settings Correct
6. Windows Update (repeat as necessary)
   - Common Error: time settings
   - May need to delete Update Contents, see note below
7. Windows Settings and Tasks
8. Install additional software as needed (copy all .exe files to Downloads Folder first using USB)
   - May need to create a Software Installation Folder and USB Key

Reminder: machine may need multiple restarts

CAUTION: Complete the Installation, then update the machine, then register WINDOWS with Product Key
- OPTION: register windows by phone, see folder for more details

Reminder that changes the "rules" about updates (NOT WINDOWS mandatory updates, or other OS Updates)
- "Only update individual programs when you have time to test the entire machine"
- Sometimes an update causes other programs to fail
- If an entire machine fails, then the most stable versions of all software must be used
- "Which is the way you had it before. Ensure you have all installation files of your most recent stable version."

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

### Run Windows Update

**Troubleshooting: Deleting Windows Update Contents**
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

ReRun Windows Update

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
- See Power Teacher (Power School / Progress Module / Click Here to install preferred Java Version)
- Ensure Environmental Variable (Pathway) is set properly
  - CAUTION: no direct error message if typed with error, be careful and check typing twice

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

### Video Player: vlc-3.0.3-win64.exe, 20180613
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

### 7 Zip: 7z1805-x64.exe, www.7-zip.com, 20180614

### GitHub Desktop: GitHubDesktopSetup.exe, https://desktop.github.com/, 20180614

### Other Browsers for Testing CSS files

See Last Pass for up dated List
https://lastpass.com/misc_download2.php

Chrome: see above

Firefox: Firefox Installer.exe, https://www.mozilla.org/en-US/firefox/new/, 20140613

Opera: OperaSetup.exe, https://www.opera.com/, 20180613
  - Might be unsupported after 201808

Unknown: mx5.2.3.2000.exe, 20180614

Internet Explorer: installed with Windows

### WYSIWYG (What You See is What You Get) Text Editors
- Test these with Hello World Program in Chrome, see index.html
- Student Editor
  - Notepad++: npp.7.5.6.Installer.x64.exe, https://notepad-plus-plus.org/ ,20180614
- Professional Editors
  - Atom: AtomSetup-x64.exe, Version 1.27.2, https://atom.io/, 20180614
  - OPTIONAL: Visual Studio Code, https://code.visualstudio.com/

Installing and Personalizing Atom (Optional Settings and Additions)
- Completely customizable ... you create your environment not based on proprietary choices
- "Why Atom": open multiple projects in one window
- See the Flight Manual: http://flight-manual.atom.io/
  - Set-up Section is good, use this with Video 1 below
  - Note: Tree View has parent, child, and sub notes
- Video #1: https://www.youtube.com/watch?v=U5POoGSrtGg
  - See the Rest of this Channel to get some ideas for using Atom
- Note about Signing in to GitHub through Atom
  - Must review permissions on a regular basis
  - For further ideas see: https://help.github.com/articles/authorizing-oauth-apps/

Suggestions for packages
- Already installed: Built In Plug-In for Spelling
  - adds suggestions for variables already spelt in code, nice feature
- Git-plus: allows you to use Git in Atom without the (CMD) Terminal or GitHub Desktop
- Navigating in Atom made easier
  - File-icons
  - Mini-map
- Atom-beautify: for formatting
- Linter: finds common code errors, for example unclosed HTML Tags
- Colour-picker: adds colour picker to Atom, similar to Processing-JAVA IDE
  - Do Not need to use Google for Hexadecimal Colour Searching

Additional Packages and themes: https://atom.io/packages

### Java: Processing-Java, Processing-Android, and Pure Java
**CAUTION: this installation has a few steps and should be done last**
  - used on all machines

Note: JDK Version from Oracle should be already installed or verified, reference above

Program Installation Overview
- Processing: processing-3.3.7-windows64.zip, https://processing.org/download/, 20180614
- Android Studio (Uses Pure Java, CS30), https://developer.android.com/studio/
  - NOTE: Android Studio's SDK GUI Manager made Processing Installation easier, not necessary as of 20180614
  - When installing SDK, update JDK and Manager for KitKat, Android 4.4 (most legacy that is tested to work)
    - Installing all OS Options will use a lot of Hard Drive Space (>200Gb), be careful about your overall hard drive size
  - Note: when choosing an Android OS, choose the one on your device, search your device to locate what is installed and updated

Processing Installation
- Download ZIP File, extract with 7-Zip (already installed above)
- Move folder to Program files (C:\Program Files)
- Create shortcut to processing.exe in the Start Menu
  - https://www.howtogeek.com/howto/6463/stupid-geek-tricks-how-to-open-the-start-menu-folder-in-windows-7/

Customize Processing Java & Android (Download Packages using Contribution Manager)
- Menu: Sketch / Import Library / Add Library
- Libraries to Add (Note: additional instruction websites for some libraries available, reference below, last accessed 20180631)
  - Note: all libraries have instructions available on Processing.org/reference
  - Ketai (http://ketai.org/, text available from Pragmatic Book Shelf, "Rapid Android Development")
  - Minim (http://code.compartmental.net/minim/, additional YouTube Videos, etc. are available)
  - OpenCV (https://opencv.org/)
  - Interfascia (http://interfascia.berg.industries/)
  - Sound (Built in Processing Library: https://processing.org/reference/libraries/sound/)
- Modes to Add: Android Mode (note: requires Processing 3.3.7, 20180613)
- Tools to Add
  - Git Manager
  - Upload to Pi
- Examples to Add (Accessed through Menu: File / Examples)
  - Note: 20180614 some examples were not available
  - Getting Started with Processing
  - Learning Processing 2nd Edition
  - Processing for Android
  - Processing Handbook 2nd Edition
  - The Nature of Code

Restart might be required: close program and restart Processing using Start Menu shortcut
- Ensures all libraries, etc., added to correct folder in Program Files
- Able to Open c:\Program Files \ processing-3.3.7
- Navigate to Libraries folder and visually verify package installations

Other Libraries Exist: Processing.org/reference
- Search for these and read about what they do, then start to use them
- Google Search these to see if additional websites or texts exist
- Note: if a text exists, able to Google Search filetype:pdf to see if reading is acceptable before purchasing and supporting the author

*Processing-JAVA Mode is now ready for use*

**Following Instructions require Android Device for further installation and configuration**

Processing-Android Mode Dependencies and Testing
- MUST have android device with USB Debugging Enabled (Google Search to enable this on your device, if necessary)
  - Double CAUTION: rooting a device has had issues in the past (if you know what rooting is, then you are also aware of the issues)
- Instructional Website & Text References: http://android.processing.org/

Processing IDE: change Java Mode to Android Mode
- Once Android Mode selected, follow prompts
- Download SDK Manually (does not need Android Studio SDK GUI Manager, 20180613)
- Accept Licenses
- Verify pathway of installation (record this! you might need it later)
  - Example: C:\Users\MercersKitchen\Documents\Processing\android\sdk\extras\google\usb_driver
  - Example: C:\Users\Mark\AppData\Local\Android\sdk
- Note this will take a while, be prepared
- Select Java Mode again: will need to restart machine and Processing-Java is better to start from here
- Close Processing IDE

Android Driver Installations: doubleClick to install, may need to Unzip first
- Install Samsung Driver first, then Universal Driver (worked as of 20180615)
  - Optional: only install the Universal Driver until you have a Samsung device
- For Samsung install: SAMSUNG_USB_Driver_for_Mobile_Phones.exe (Last Accessed 201502)
  - http://downloadcenter.samsung.com/content/SW/201410/20141017131240597/SAMSUNG_USB_Driver_for_Mobile_Phones.exe?utm_source=gsmmaniak.pl&utm_medium=artykul&utm_campaign=techmaniak.pl
- For other Android Devices: UniversalAdbDriverSetup.msi (Last Accessed 20180614)
  - Universal ABD Drivers: https://adb.clockworkmod.com/
  - Caution: Windows "doesn't believe" this is a safe driver, doesn't want a virus; these steps used successfully 20180615
  - Open "Devices and Printers" (Windows 7)
    - Ensure device is plugged in and USB Debugging is enabled
  - Under "Device Properties", navigate to where driver software can be loaded/changed/seen
  - Click "Update Driver"
  - Follow the Prompts and navigate menus
    - "Browse My Computer" and "Let me pick..."
  - Select device you have
  - Click on all and load the whole list: clockworkmod
    - Future Research: read how and why to do this
    - In the left pane: sorted by manufacture, look for clockworkmod
  - INSTALL IT :)
    - Now: device will freak out and implode :) (Quote from student who helped write instruction list)
  - After device reassembles itself, popup asking permission for this computer to debug via USB
  - Click YES

Restart Entire Machine, ensures all pathways are correct (especially environmental pathways)
- Troubleshooting Example: Set Path to Android SDK Path (in C:\Users\Mark\AppData\Local\Android\sdk)

Restart Processing-Android (reselect Processing-Android)
- Normal Processing IDE Boot: no prompts for downloads, etc. (besides optional updates)
- Change AVD API to that of device (i.e. current Android OS of the device)
- Change Target Phone device
- Processing-Android ready to side-load to device

Download and Run Processing-Android "Hello World" Sketch (Sketches are name for Processing coded programs, from Processing)
- See AcerHelloWorld
- Run on Device (but not on Emulator)
- Remember about device permission (not activated on this Hello World Sketch, but might be needed in future)
- Ensure device is connected and you can see it in Processing-Android Menu: Sketch
- Run the Sketch on the Device
- Play with the Touch Screen Program
- Stop the Sketch and Power-down device to "Dismount the Drive" (currently Task-bar does not have dismount function)

Final Test ... Finally: Testing Pure JAVA (Windows 7 or Windows 10)
- See Testing JavaJDK
- Move Folder to Pure Java Programs in My Documents (or where you will store Pure Java Files)
- Shift-Right-Click on the folder, "Open command window here"
``` CMD or PowerShell
javac HelloWorld.java
java HelloWorld
```

---

Additional Software and Website List
- www.ubuntu.com
- www.canonical.com: for Ubuntu software updates
- SlackSetup.exe for messaging and Social Networking

Search Engines: Google's V8, Bing (for research and to find updates)

---

## Installation Instructions for a WAMP Server
See Folder and Notes from Installation
- Not used on all machines unless writing PHP, etc.

**Complete this after testing WAMP Server**

Incomplete Instructions
- WAMPServer: wampserver3.1.0_x64.exe
- http://www.wampserver.com/en/
- Composer for Windows: Composer-Setup.exe
- Extra Files: cacert.pem

---

# Previous Software Notes Not Deleted Yet

### GitHub Classroom
- Must install Atom (AtomSetup-x64.exe) First (or Notepad++, etc.)
- Install Git-2.16.2-64-bit.exe (enable Atom or WYSIWYG choice)
- Install GitHub Desktop

### Robotics Software and Additional Notes
Fritzing: http://fritzing.org/home/
- Run the .exe
- Allow to run update in the background, will be notified
- Allow to do a file clean
- Allow to do a new parts update

Installation for VEX
Install VEX Robot C
Install this one: VEX Driver Installer 64-bit
Upgrade & Repair, will case Error 1316 (known and OK)
VEXNet Firmware Upgrade Utility: setup
VEXNet Key Firmware Upgrade Utility: setup

---

# Additional Troubleshooting Notes

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

# Future Ideas to Include
List of Ideas
- Using Older machines and "lighter OS"
- Ubuntu Installation (Connections to Cisco Academy Courses)
- RPI setup and Raspbian Installation (including WiFi Configuration)
- Completing a Dual Boot
- Separate List of Programs (currently all programs have usage in different courses on a developers machine)
  - For Example: testing installations of new programs occur in a virtual machine
