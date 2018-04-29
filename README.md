MBPUP Linux - remasterable live linux desktop - a fork of Bionic Dog (Ubuntu) 18.04
=

MBPUP Linux is a linux disro remastered by MBinnun, based on the BionicDog Linux distro (which is itself a remastering of Ubuntu Bionic Beaver 18.04).

Unlike BionicDog and any other Puppy-like distros, MBPUP supplies a full featured Lubuntu (Ubuntu + LXDE environment) and intended to run on today's hardware.

Its goal is to have a fully functional desktop from a live CD/USB containing fully supported firmware, but also to be lightweight and super easy to remaster (so you'll be able to create as many "versions" of your desktop as you like).

Another advantage of MBPUP is the ability to install a functional desktop "as is" to the hard drive (either a standard installation or a frugal one).


** Note: because the ISO images of the release were too large to store on a git, I had to store them on my google drive. Feel free to download from there (links are attached).

Download MBPUP 32bit version 1.0 ISO image from:
-
https://drive.google.com/open?id=1scuMWt2z6605jwv3_xIzPvm5OhndMyhx

Download MBPUP 64bit version 1.1 ISO image from:
-
https://drive.google.com/open?id=1TYxeIz3ReJCHHZoQn9MdtML43x2YTEqH

---------------------------------------

MBPUP-VM - Portable virtualization distro
=

Ever wanted to run a VM on a new machine without installing any additional software? Now you can!<br />
MBPUP-VM is an MBPUP distro with embedded virtualization software such as VMware-Player, VirtualBox and QEMU.<br />
Only run the live system and you'll able to run any VM you like without any additional installation.

** Note: the kernel on this release was updated to 4.15.0-20 and linux-headers are installed.

Download MBPUP-VM version 1.1 ISO image from:
-
https://drive.google.com/open?id=1LVT792OPPVGmv4GVABHvIFLd2syyuGMW

----------------------------------------

Known issues:
=
On the 64bit distros of MBPUP, sometimes the PcManFM file manager crashes immediately after the user login.
-
**Resolution:**<br />run **sudo rm /var/crash/\*** from the terminal and reload PcManFM.<br />You're not supposed to experience additional crashes till the end of the session.

**Another option:**<br />use *Nautilus* as your primary file manager.
