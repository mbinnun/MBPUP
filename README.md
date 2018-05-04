MBPUP Linux - remasterable live linux desktop - a fork of Bionic Dog (Ubuntu) 18.04
=

MBPUP Linux is a linux disro remastered by MBinnun, based on the BionicDog Linux distro (which is itself a remastering of Ubuntu Bionic Beaver 18.04).

Unlike BionicDog and any other Puppy-like distros, MBPUP supplies a full featured Lubuntu (Ubuntu + LXDE environment) and intended to run on today's hardware.

Its goal is to have a fully functional desktop from a live CD/USB containing fully supported firmware, but also to be lightweight and super easy to remaster (so you'll be able to create as many "versions" of your desktop as you like).

Another advantage of MBPUP is the ability to install a functional desktop "as is" to the hard drive (either a standard installation or a frugal one).


***Release notes of version 1.2***<br />
https://github.com/mbinnun/MBPUP/releases/tag/V1.2


Download MBPUP 32bit version 1.2 ISO image:
-
https://github.com/mbinnun/MBPUP/releases/download/V1.2/MBPUP32-v1.2-20180501.iso

Download MBPUP 64bit version 1.2 ISO image:
-
https://github.com/mbinnun/MBPUP/releases/download/V1.2/MBPUP64-v1.2-20180502.iso

---------------------------------------

MBPUP-TVDESK - OS for streamers or office desktops
=

Need additional desktop functionality?<br />
MBPUP-TVDESK includes extra tools, such as: LibreOffice, Gimp, VLC and KODI.

Download MBPUP-TVDESK 32bit version 1.2 ISO image:
-
https://github.com/mbinnun/MBPUP/releases/download/V1.2/MBPUP32TVDESK-v1.2-20180503.iso

Download MBPUP-TVDESK 64bit version 1.2 ISO image:
-
https://github.com/mbinnun/MBPUP/releases/download/V1.2/MBPUP64TVDESK-v1.2-20180503.iso

---------------------------------------

MBPUP-VM - Portable virtualization distro
=

Ever wanted to run a VM on a new machine without installing any additional software? Now you can!<br />
MBPUP-VM is an MBPUP distro with embedded virtualization software such as VMware-Player, VirtualBox and QEMU.<br />
Just run the live system and you'll able to load any VM you like without any additional installation.

**Note:** The kernel on this release is updated to 4.15.0-20 and linux-headers are installed.

Download MBPUP-VM version 1.2 ISO image:
-
https://github.com/mbinnun/MBPUP/releases/download/V1.2/MBPUP64VM-v1.2-20180502.iso

----------------------------------------

Known issues:
=
On v1.2 release, sometimes PcManFM file manager crashes immediately after the user login.
-
**Resolution:**<br />Run **sudo rm /var/crash/\*** from the terminal and reload PcManFM.<br />You're not supposed to experience additional crashes till the end of the session.

**Workaround:**<br />Use *Nautilus* as your primary file manager.
