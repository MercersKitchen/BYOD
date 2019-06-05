# Specific Instructions for Cyber Security Computers
Networking Instructions Specific for 6560 & 6570b Laptops

Advanced Instructions for Reinstallation of Windows: <a href="https://docs.google.com/document/d/1JEimk9RuD1SNG_4g3HX1gruRYhk876r81y6ppanpyQg/edit?pli=1">Google DOCs Version, more private version, copied below</a>
- WORD Version, see <href="">Repo</a>
- PDF Version, 20190605, see <href="">Repo</a>

# Anthony's Instructions

Anthony’s Automation for Drivers and Software
Steps by Anthony
Verification by Ralph

Boot the laptop into the Windows 10 installer usb. (If you don’t have this usb, make it)
- Rufus
- Windows ISO Downloader Program (https://www.microsoft.com/en-ca/software-download/windows10)
- Download through Chrome, like a Mac:
  - Right Click / Inspect / Console / 3-dots / Network Conditions / User Agent / CLick Off Select Automatically / Select Safari - Mac / Leave COnsole Open, Refresh / Try Downloading WIndows 10, Oct

Run the installer

When it asks for a product key give it the product key found on the windows oem label somewhere on the laptop (usually on the bottom somewhere)

If this drive has an old operating system make sure to delete every partition until the partitioner says everything is “Unallocated space”

Once it is done installing begin doing the setup

During the setup you will be asked to sign-in to a Microsoft account. You want to select “Offline account” instead. The username should be MercersKitchen. The password should be “???”.  (change to [password] )

During the account setup it’s going to ask for some security questions. Here is what you want to put in:
- What’s the name of the city where you were born? The answer should be: Edmonton
- What’s the name of the city where your parents met? The answer should be: Edmonton
- What’s the name of the first school you attended? The answer should be: Queen Elizabeth

After the account setup you it’s going to ask you a bunch of privacy questions just agree to all of them (A lot of them are disabled later)

Once at the desktop you’re gonna want to first and foremost turn off and unpin a couple taskbar things. Right click on the taskbar and turn off “Show Task View button” and “Show People button”. For the unpinning, unpin the mail app, windows store, and microsoft edge.

Type into the search: “File explorer options”. Once that is open select “Show hidden files, folders, and drives”, turn off “Hide extensions for known file types”, and turn on “Launch folder windows in a separate process”. Once done, close the window.

Type into the search: “Start settings” if you the search isn’t showing this you will have to open the Settings app and then search for the start settings in there. Once at the start settings, turn off “Show suggestions occasionally in Start”

In that same start settings window select “Taskbar” and turn off “Replace command prompt with…”

Type in search: “Group policy” and open it. Under “Computer Configuration” go to the following place, “Administrative Templates>Windows Components>Cloud Content” and switch “Turn off Microsoft consumer experiences” to Enabled

Still in group policy, go to “Administrative Templates>Windows Components>Search” and switch “Allow Cortana” to Disabled. Once done, close the window.

In the Drivers folder there are two folders that are titled BIOS Update. Each of them have a different model number in brackets. You need to run the installer in the folder that matches the model number on the computer. Example: BIOS Update (6570b) you will run that installer for a computer that has the model number 6570b.

On the USB, open the “SDI_RUS” folder and run “SDI_x64_R1904.exe”. Give it admin rights. Select the “Create a restore point” and “Reboot PC after installation” checkboxes. Then, select the Select all button and then click Install. The program will install the best drivers available for this machine at the time of this document’s creation.

Now for the software, go back to the USB and open the folder called Software. In this folder there will be many setup programs. You’ll want to run all of them, some require internet access so you will have to connect to the wifi at this point. (Note about the software: Some setups may be out of date when ran and the programs will have updates available on opening them)

While running all the setup utilities make sure that the setup programs do not have desktop shortcuts selected.

Notes regarding specific program setups:
- Processing: Processing doesn’t have an installer. You need to copy the processing folder to C:\Program Files. Once that is done copying you will then want to create a shortcut to it on the desktop that will open the file processing.exe. You now need to copy this shortcut to two places, they are: C:\Users\Public\Public Desktop and C:\ProgramData\Microsoft\Windows\Start Menu\Programs
- Git: Git has a lot of options to choose from during setup. In the first set of options turn off Windows Explorer integration. After that, in the dropdown select the option Use the Nano editor by default. In the next screen make sure Git from command line and also from 3rd-party software is selected. Make sure Use the OpenSSL library is selected. Make sure Checkout Windows-style, commit Unix-style line endings is selected. Select Use Windows’ default console window.
- ShareX: Just make sure every option except for Create a send to shortcut is not selected.
- VMware Player: Turn on the Enhanced Keyboard Driver option. Turn off the Check for product updates on startup and the customer experience improvement program options. Turn off the Desktop shortcut option.
- Wireshark: Wireshark is a very big installer, it’s got lots of options. Turn off the User’s Guide option. Turn on the Install USBPcap option. This installer actually opens two other installers that you will have to run through. The options for one of those installers are:
- Npcap: Turn on the Support raw 802.11 traffic option.
- Open the wifi settings go into Manage known networks, select Edmonton Public Schools and click Forget
