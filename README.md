# Emulated-Android-on-Kali-Live-USB
this is a fast easy way to emulate a full android on a kali live usb boot that has persistence added. it also includes adding notepad++

another option is using a phone you own and running scrcpy  

my setup is:

a laptop with no hard drive installed
kali-everything live on 128 GB flash drive with persistence

kali-tweaks:
i have all distributions
i have all tools
this is not all required..but what my current package is

i ran
sudo winefile (also not positive this is required but i do it for access to notepad ++)
then ran the two install files requires (note you have to add sudo at the statrt of the list and after the &&) just copy paste will not work

then i downloaded notepad++

https://github.com/notepad-plus-plus/notepad-plus-plus/releases/download/v8.5.3/npp.8.5.3.Installer.x64.exe
---------

open terminal in downloads and i check to make sure i have the correct name of the file
~~~~~
ls
~~~~~
~~~~~~
sudo wine npp.8.5.3.Installer.x64.exe
~~~~~~
install and the file is left in the root folder

virtualbox:

~~~~~~~~
sudo apt update && sudo apt upgrade -y
~~~~~~~~
~~~~~~~~
sudo apt install virtualbox -y && sudo apt update 
~~~~~~~~

next download 
android-x86-8.1-r6.iso (32bit)

from 

https://www.fosshub.com/Android-x86-old.html?dwl=android-x86-8.1-r6.iso
------------

open console at /home/kali
~~~~
virtualbox
~~~~
(dont run this with sudo because it will make a second file in the root and cause problems)

a screen will appear
once in this screen your mouse and keyboard are locked inside the virtualbox
to get controll of your mouse or keyboard outside of the virtualbox press the "Ctrl" button on the RIGHT side of the keyboard

click new
enter a name 
ISO image (leave empty)
type (select other)
version (select other/unknown)

pre allocate what ever size you want
i just did 20GB and click EFI mode

start the machine and it asks for iso file. 

add the download iso of android x86 and click (mount and restart)

install android x86 

you will need to make a partition.

(this is confusing because it says your making a parition at /dev/sda1 [not the case] what it is doing is making a partition at /virtualbox/dev/sda1 pm the virtual hard drive we made in the previous step)

click new and the size it is defaulted at is correct. 
select bootable and press enter so the partition is bootable
select write 
then exit

format ext4 and select yes for read/write for a rooted phone

it takes a short time to install and asks if you want to boot.

when it boots. you can skip the set up 
there are two default options for the home screen (I prefer the top option)

open the phone options tab and find android x86 and select the 2 options that are not activated

then you can turn on wifi and finish setup how ever you decide

you can also plug in a micro sd card at this point and format it for extra storage...i sugest adding as portable storage and not internal... any time i try to add my 2TB micro SD as internal storage the system freaks out. 

the android is now set up and with persistence added if when you shut down you select the top option of the 3 listed



some extra notes:

when clicking things in the settings .. click the words next to the slide button and not the button it self

download fdroid from chrome and activate all repository

when searching in these app stores keep it simple with 1 word or a few letters and dont use spaces

after fdroid updates the respoitories search in fdroid for neo   (neo store is the one to select)

when neo store is downloaded then activate all the repositories in Neo Store and use that for your app store





hack the world

donations can go two ways. check out my site for wholesale electric scooters.. and such
https://easy-flow-riders.square.site
----------------
