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

**NOTE** : Create links in Start Menu and leave Desktop Clean

---

## For Computers using SchoolZone (all) or PowerTeacher
### Ensure JDK matches PowerTeacher Java Version
- Currently 8u121, 20180613
- See PowerTeacher (PowerSchool / Progress Module / Click Here to install)
- Ensure Environmental Variable (Pathway) is set properly
  - CAUTION: no direct error message if typed with error

---

## For computers not using EPSB Imaging services OR Install Instructions for specific programs

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

###

---

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
