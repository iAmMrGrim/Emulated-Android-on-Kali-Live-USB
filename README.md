# Emulated-Android-on-Kali-Live-USB

simple answer: run androidx86_32.iso

the 64 is not the way

this is a fast easy way to emulate a full android on a kali live usb boot that has persistence added. it also includes adding notepad++

notes and extra help is at the end of the page

________________________
virtualbox:
~~~~~~~~
sudo apt update && sudo apt upgrade -y
~~~~~~~~
~~~~~~~~
sudo apt install virtualbox -y 
~~~~~~~~
~~~~~~~~
sudo apt update && sudo apt upgrade -y
~~~~~~~~
________________________
android x86 download (32 bit)

old version (faster)

https://osdn.net/projects/android-x86/downloads/69704/android-x86-8.1-r6.iso/
------------
________________________
new version (slower)

https://www.fosshub.com/Android-x86.html?dwl=android-x86-9.0-r2.iso
------------
________________________
open console at /home/kali
~~~~
virtualbox
~~~~
____________________
click new

name: Bitch Tits Bob

ISO image (default)

type (other)

version (other/unknown)

create
________________________
pre allocate size (yes)   

[the size you choose on this page determines the storage space the phone has and will take up part of the space on your usb drive]

EFI mode (yes)
________________________
start Bitch Tits Bob

add the android x86 iso (mount and restart)
________________________
INSTALL ANDROID X86

make a partition (n)(enter)

gpt (no)

new (enter)(enter)

bootable (enter)

write (enter)

exit (enter)
________________________
format (ext4)

read/write (yes)
________________________
the android is now set up and with persistence added if when you shut down you select the top option of the 3 listed

________________________
Turning that into nethunter

turn on extensions
~~~~~~~~~~~~~~~~~~
sudo apt install -y --reinstall virtualbox-guest-x11
~~~~~~~~~~~~~~~~~~~
The nethunter app download

https://store.nethunter.com/NetHunterStore.apk
-----------------------

this is not a speedy process. any time the emulator is acting up reboot into kali live with out persistence and run 

~~~~~~~~~~~~~~~~~~~~
sudo fsck /dev/sdc3
~~~~~~~~~~~~~~~~~~~~

then when you re boot into android run the updater instead of loading into the phone (or debug)

in the nethunter app switch to catagories. DONT INSTALL PRIVILEGED EXTENSIONS...

install the termux stuff and the stuff in the catagory with the nethunter install.. open them as you install them and set up each one. 

load into termux and run


~~~~~~~~~~~~
pkg up -y
~~~~~~~~~~~~
~~~~~~~~~~~~
pkg install root-repo
~~~~~~~~~~~~
~~~~~~~~~~~~
pkg install x11-repo
~~~~~~~~~~~~
~~~~~~~~~~~~
termux-setup-storage
~~~~~~~~~~~~
~~~~~~~~~~~~
termux-wake-lock
~~~~~~~~~~~~

follow the instructions to set up the rootfs in nethunter terminal

________________________
BONUS:
________________________
notepad++ download

https://github.com/notepad-plus-plus/notepad-plus-plus/releases/download/v8.5.3/npp.8.5.3.Installer.x64.exe
----------
install wine 
~~~~~~
sudo winefile
~~~~~~
open terminal in downloads
~~~~~~
sudo wine npp.8.5.3.Installer.x64.exe
~~~~~~
the installed file is left in the /root folder (making a link to it and putting it on your desktop is helpful)

________________________
NOTES:
________________________
my setup is:

laptop with no hard drive installed

kali-everything live on 128 GB flash drive with persistence

kali-tweaks: I have all distributions and all tools

(this is not required..but what my current package is)
________________________
~~~~
virtualbox
~~~~
(do not run this with sudo because it will make a second file in the root and cause problems)
________________________
when making the partition cfdisk says you are making the partition at /dev/sda1 but this is not correct.

the partition is being made at /virtualbox/dev/sda1 on the new virtual hard drive we created
________________________
once you click the virtualbox screen your mouse and keyboard are locked inside the virtualbox

to get controll of your mouse or keyboard outside of the virtualbox press 

"Ctrl" button on the RIGHT side of the keyboard
________________________
when clicking things in the settings .. click the words next to the slide button and not the button it self
________________________
download fdroid from chrome and activate all repository

when searching in these app stores keep it simple with 1 word or a few letters and dont use spaces

after fdroid updates the respoitories search in fdroid for neo   (neo store is the one to select)

when neo store is downloaded then activate all the repositories in Neo Store and use that for your app store
________________________
you can plug in a micro sd card and format it for extra storage...

I sugest adding as portable storage and not internal...

Any time i try to add my 2TB micro SD as internal storage the system freaks out. 
________________________
wine 

running the two install files wine requires (note: just copy paste will not work)

you have to add sudo at the start of the command and after the && where the second command begins
________________________
another option is using a phone you own and running scrcpy  
https://github.com/Genymobile/scrcpy
----------------
________________________
hack the world
________________________
donations can go two ways. check out my site for wholesale electric scooters.. and such

https://easy-flow-riders.square.site
----------------

