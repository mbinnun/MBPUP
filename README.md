MBPUP Linux - remasterable live linux desktop - a fork of Bionic Dog (Ubuntu) 18.04
=

MBPUP Linux is a linux disro remastered by MBinnun, based on the BionicDog Linux project (which is itself a remastering of Ubuntu Bionic Beaver 18.04).

Unlike BionicDog and any other Puppy-like distros, MBPUP supplies a full featured Lubuntu (Ubuntu + LXDE environment) and intended to run on today's hardware.

Its goal is to have a fully functional desktop from a live CD/USB containing fully supported firmware, but also to be lightweight and super easy to remaster (so you'll be able to create as many "versions" of your desktop as you like).

Another advantage of MBPUP is the ability to install a functional desktop "as is" to the hard drive (either a standard installation or a frugal one).


***Remaster live and easily***<br />
The live system of MBPUP is remasterable even without touching the hard drive! All you need to do is:<br />
1) Boot the live system, install packages and do any changes you want - live.
2) Afterwards, run the *Remaster live system* script - so it will generate a SquashFS file for you.
3) Edit the original ISO with IsoMaster or any other ISO editor. Overwrite **01-filesystem.squashfs** from the casper directory with your own generated SquashFS.
4) Save the ISO, and that's it! You should now have a live cd of your own customized system.


***Release notes of version 1.3***<br />
https://github.com/mbinnun/MBPUP/releases/tag/V1.3

***Release notes of version 1.2***<br />
https://github.com/mbinnun/MBPUP/releases/tag/V1.2

***It is very recommended to read the known issues before running the system***<br />
<a href="#issues">Read known issues</a>


Download MBPUP 64bit version 1.3 ISO image:
-
https://github.com/mbinnun/MBPUP/releases/download/V1.3/MBPUP64-v1.3-20180512.iso

Download MBPUP 32bit version 1.3 ISO image:
-
https://github.com/mbinnun/MBPUP/releases/download/V1.3/MBPUP32-v1.3-20180512.iso

<img src="https://github.com/mbinnun/MBPUP/blob/master/mbpup_screenshot.png" alt="MB-PUP screenshot" />

---------------------------------------

MBPUP-TVDESK - OS for streamers and office desktops
=

Need additional desktop functionality? Looking for an ultimative OS for a streamer?<br />
MBPUP-TVDESK includes some built in extra tools, such as: LibreOffice, Gimp, Google Chrome, VLC and KODI.

Download MBPUP-TVDESK 64bit version 1.3 ISO image:
-
https://github.com/mbinnun/MBPUP/releases/download/V1.3/MBPUP64TVDESK-v1.3-20180512.iso

Download MBPUP-TVDESK 32bit version 1.3 ISO image:
-
https://github.com/mbinnun/MBPUP/releases/download/V1.3/MBPUP32TVDESK-v1.3-20180512.iso

---------------------------------------

MBPUP-TVDESK with Gnome Desktop
=

Not familiar or unsatisfied with the LXDE environment?<br />
This version of MBPUP-TVDESK is built with Gnome desktop and looks as same as the original Bionic Beaver release (Gnome 3, that reminds the Unity desktop).

Download MBPUP-TVDESK 64bit version 1.3 with Gnome desktop:
-
https://github.com/mbinnun/MBPUP/releases/download/V1.3/MBPUP64TVDESK-v1.3-GNOME-20180517.iso

---------------------------------------

MBPUP-VM - Portable virtualization environment
=

Ever wanted to run a VM on a new machine without installing any additional software? Now you can!<br />
MBPUP-VM is an MBPUP distro with embedded virtualization software such as VMware-Player, VirtualBox and QEMU.<br />
Just run the live system and you'll be able to load any VM you like without any additional installation.

**Note:** The kernel on this release is updated to 4.15.0-20 and linux-headers are installed.

Download MBPUP-VM version 1.3 ISO image:
-
https://github.com/mbinnun/MBPUP/releases/download/V1.3/MBPUP64VM-v1.3.1-20180520.iso

---------------------------------------

MBPUP-SRV - A webserver to-go
=

MBPUP-SRV is a porable (but complete) live web server!<br />
MBPUP-SRV is coming with LAMP (Apache + MySQL + PHP) preinstalled.<br />
In addition, it also contains: server administration GUI (WebMin), mailserver (Postfix + DoveCot), web mail GUI (RoundCube) and MySQL administration GUI (PhpMyAdmin) which all run out of the box.<br />
MBPUP-SRV integrates an OpenSSH service with a VNC server (for remote control on the desktop mode).

Download MBPUP-SRV version 1.3 ISO image:
-
https://github.com/mbinnun/MBPUP/releases/download/V1.3/MBPUP64SRV-v1.3-20180512.iso

---------------------------------------

MBPUP-DEV - The ultimative linux distro for a developer
=

MBPUP-DEV provides a pefect environment for the average developer.<br />
It includes many programming tools and development IDEs: Eclipse, Android Studio, Core Linux Dev Tools (gcc, g++, python), Java (both OpenJDK and Oracle), Free Pascal Compiler, MonoDevelop, Git, NodeJS, Angular CLI, Visual Studio Code, Gimp (for graphical design) and a lot more.<br />
All these tools are ready to run, of course, out of the box on the live system.

**Note:** The download file is big (about 3 gigabytes), due to the very large amount of tools that are installed.

Download MBPUP-DEV version 1.3 ISO image:
-
https://drive.google.com/open?id=169JUTLmOBqK4Qq4PZuDD9hUv7mSPS1C4

----------------------------------------

<a name="issues"></a>Known issues:
=
On some occations, PcManFM file manager crashes immediately after the user login.
-
**Resolution:**<br />Simply run **sudo rm /var/crash/\*** from the terminal and reload PcManFM.<br />You're not supposed to experience additional crashes till the end of the session.

**Workaround:**<br />Use *Nautilus* as your primary file manager.

On some occasions, after a standard installation to the hard drive - grub4dos does not find "/boot/vmlinuz" and startup fails!
-
**Resolution:**<br />When grub4dos appears, press &lt;TAB&gt; to edit the grub entry just before it boots.<br />Replace **/boot/vmlinuz** with **/boot/vmlinuz-4.15.0-20-generic** on the "kernel" option, and it will boot successfully.<br />After the successful boot, run **sudo nano /ment.lst** from terminal and change this entry permanently.<br />Done, problem solved!<br /><br />
***Note:*** The vmlinuz issue has been fixed on version 1.3.

On some occasions, when trying to run a standard installation from a USB flash drive - it says "could not find /mnt/sdb1" and the installation does not start.
-
**Resolution:**<br />When booting from USB, when the isolinux menu appears press &lt;TAB&gt; to edit the menu entry just before it boots.<br />Remove **noauto** from the line and boot. The standard installation will run successfully this time.<br /><br />
***Note:*** The "noauto" flag has been removed from the ISO files on version 1.3, therefore this issue has been resolved.

Hey, where did all my mountable devices go - on version 1.3?
-
**They did not.**<br />On version 1.3 they are pre-mounted by the root system.<br />You should find all mounted devices under **/mnt/**.

After running the script that turns the standard installation into a "real Ubuntu", the swap partition does not automatically mount on boot any more.
-
**Correct.**<br />This is because turning the system into a "real ubuntu" removes the porteus boot, so mounting devices will rely on /etc/fstab from now on.<br /><br />
**Resolution:**<br />Run **gnome-disks** from terminal. When the GUI shows up, select the swap partition. On its settings menu click on **edit mount options**. On mount options, turn off the "Automatic Mount Options" switch and make sure the "Mount at startup" checkbox is checked. Click OK, then reboot.<br />
Done, the swap partition will automatically mount.

After a standard installation, booting from the hard drive is REALLY slow.
-
That happens if the *initrd* was not re-generated after the installation from some reason.<br />There's a script on the desktop that fixes the issue. Make sure to run it from a hard drive session only, and not from a live session.<br /><br />
***Note:*** DO NOT run the script if you've already turned your standard installation into a "real Ubuntu".

A newly created user invokes an annoying message on startup.
-
**Resolution:**<br />From terminal: **nano ~/.profile** -> comment out the last line (the one with 'mesg') -> save -> done!<br />
The annoying message will not appear on the next login.

Only on the Gnome version, I can't load the desktop mode as usual with 'service lightdm start'.
-
**Correct.**<br />The GDM-3 desktop manager replaces the LightDM manager (only) on the Gnome version.<br /><br />
**Resolution:**<br />Run **service gdm3 start** instead, then login as "administrator" with the regular sudo password.

On the Gnome version, a newly created user does not log in.
-
**Resolution:**<br />Try choosing **Gnome Xorg** session type instead of "Gnome" on the GDM3 login screen.<br />It should log in successfully without problems.

On the VM version, I can't remove the extension pack on virtuabox (when I to try install a new one) and it shows me an error.
-
**Resolution:**<br />From terminal: **cd /usr/lib/virtualbox/ExtensionPacks/** and then **sudo rm -R Oracle_VM_VirtualBox_Extension_Pack** and then **sudo VBoxManage extpack cleanup**.<br />
It should now remove the extension pack without problems.
