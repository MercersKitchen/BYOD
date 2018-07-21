# BYOD
Computer Setup: Program Information and Settings

## Windows Installation

### Steps ... Additional Details Below
1. Download ISO Files from Microsoft
2. Create USB Installation Key
. Install WINDOWS
. Update Drives (Especially All Internet Connection Drivers)
. Ensure all BIOS Settings Correct

CAUTION: Complete the Installation, then update the machine, then register WINDOWS with Product Key

### Creating USB Installation Key
- Research these URLs
  - https://www.microsoft.com/en-us/download/windows-usb-dvd-download-tool
  - http://www.fit-pc.com/wiki/index.php/How_to_make_Windows_7_bootable_install_USB_stick
  - http://www.howtogeek.com/191054/how-to-create-bootable-usb-drives-and-sd-cards-for-every-operating-system/
- Use Rufus as option to create Bootable USB for Windows Installation
  - Use USB Rufus Key

### Using the Rufus USB Key
- Start WINDOWS as normal on the Machine
- Open Key / Double Click Setup

### Driver Information and Installation
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

### BIOS Settings
- Enable VT-X, Virtual Technology, in BIOS

# Previous Versions Notes Note Deleted Yet
### GitHub Classroom
- Must install Atom (AtomSetup-x64.exe) First (or Notepad++, etc.)
- Install Git-2.16.2-64-bit.exe (enable Atom or WYSIWYG choice)
- Install GitHub Desktop
