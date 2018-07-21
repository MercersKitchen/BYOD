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

### Steps ... Additional Details Below
1. Download ISO Files from Microsoft
2. Create USB Installation Key
. Install WINDOWS
. Update Drives (Especially All Internet Connection Drivers)
  - Note: Display driver can be an issues; also manually install additional issues as needed
. Windows Update (repeat as necessary)
  - Common Error: time settings
. Install additional programs as needed (copy all .exe files to Downloads Folder first using USB)
. Ensure all BIOS Settings Correct
. WINDOWS Defender: change settings in Options, Update and Scan
. Deal with all messages (firewall, security, backup, etc.)
.
Reminder: machine may need multiple restarts

CAUTION: Complete the Installation, then update the machine, then register WINDOWS with Product Key

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
- SATA Should be AHCI (IDE is for Windows XP and older)
- SATA Speed should be 6.0

- Change Region and Language
- Computer Name in System Properties
- Change Device Installation Settings for Drivers, to recommended

---

### Clock settings
- Ensure Clock Setting is correct
- Troubleshoot: synchronize Internet Clock to System Tray Clock

---

# Previous Versions Notes Note Deleted Yet
### GitHub Classroom
- Must install Atom (AtomSetup-x64.exe) First (or Notepad++, etc.)
- Install Git-2.16.2-64-bit.exe (enable Atom or WYSIWYG choice)
- Install GitHub Desktop
