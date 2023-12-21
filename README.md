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

[https://osdn.net/projects/android-x86/downloads/69704/android-x86-8.1-r6.iso/
](https://www.android-x86.org/download)------------
________________________

open console at /home/kali
~~~~
virtualbox
~~~~
____________________
click new

name: choose

ISO image (default)

type (other)

version (other/unknown)

create
________________________
pre allocate size (yes)   

[the size you choose on this page determines the storage space the phone has and will take up part of the space on your usb drive]

EFI mode (yes)
________________________
start the new virtual box you just made

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

