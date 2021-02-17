---
title: How to Test A Distro
nav: Try
topics: Download; Burn ISO; Boot live USB
description: The best way to learn Linux is to try it!
---

So you chose your distro.
Now let's try it out.

You can download an ISO, burn it to a USB stick, and then boot up into the live desktop without actually installing or changing your hard drive.

------------------

## Download

Most modern Linux distros are released as an ISO disk image, usually a <span class="term">live USB</span> or "live CD" meaning it can boot from the install media.

Surf over to your distro's download page to find the ISO.

One last choice you might have to make is 64-bit, 32-bit, or ARM
(i.e. the instruction set or architecture of your computer).
The options might look like:

| "64-bit", "x86_64", "AMD64" | Most computers still running are new enough to be using a 64-bit processor--so unless you know your hardware *requires* 32-bit, choose the 64-bit option. This option works for both Intel and AMD chips. |
| "32-bit", "i386", "i586" | Many distros have started phasing out 32-bit support, but you may still encounter the option for use on legacy systems. |
| "ARM", "ARMv7", "aarch64" | Support is growing for ARM processors, such as found in Raspberry Pi or newer laptops. |
{:.table .table-bordered }

Choose the appropriate download for your system, then wait.
ISO's are usually around 3GB, so it can take awhile... 

----------

## Burn a Live USB

ISO files are exact binary copies of a storage device.
You can not simply copy them onto a USB.
Instead you "burn" the image, essentially overwriting the entire media removing the existing file system.

{% capture burn %}
### Get Media

First, you need a USB drive bigger than the image you want to burn (a general purpose 8GB drive will be plenty).
Most standard USB drives will be sufficient for installing Linux, however, newer drives with faster read/write speeds will give you a better experience when using the live session (or portable desktop).

### Get Etcher

Second, you will need a disk imaging utility.
If you don't already have a favorite,
[download Etcher](https://www.balena.io/etcher/) for your system and extract the `.zip` file to access the app/installer (Linux `.AppImage`, Windows `.exe`, or Mac `.dmg`).

### Burn Image

1. Plug your USB drive into your computer.
2. Start up Etcher by clicking on the executable.
3. In Etcher, select the ISO that you downloaded.
4. Select the SD/USB (if you have only one plugged in, it will be automatically selected, Etcher will hide your main hard drives by default).
5. Click Flash! (you may need to authenticate at this point, since you are making changes to a drive)
6. Wait. Wait. Wait... (this might take awhile as Etcher burns the image then verifies the integrity)
7. Once successfully finished, remove your USB.

{% endcapture %}
{% include card.html text=burn %}

{% capture restore %}
After burning an ISO, Windows and Mac will not be able to read the USB drive, since it is formatted as a Linux filesystem.
To restore the drive to normal state (generally FAT32), you can use the official [SD Formatter](https://www.sdcard.org/downloads/formatter_4/index.html) if your system is not recognizing the full drive size when you attempt to format.
On Linux, the built in "format" utility can restore the USB.
{% endcapture %}
{% include alert.html text=restore color="secondary" %}

------

## Backup

If you are messing around with your computer, it is a good time to take some basic precautions to give you peace of mind--these are best practices that you should follow anyway!
Backup of all your files on external storage to make sure you have everything you *really* want saved in multiple stable locations.

On Windows, make a Windows Recovery Drive on a USB stick (search your system for "recovery" and the option to create a recovery drive will pop up. This ensures you can reinstall or repair Windows if necessary).
On Mac, review how to get to [macOS Recovery](https://support.apple.com/en-us/HT201314).

--------

## Boot a Live USB

To try or install your new distro from the USB, you need to boot up using the drive.
For most systems this is not the default and you will have to intervene as your computer first starts up.

The initial boot process is controlled by the BIOS or UEFI installed by your computer manufacturer. 
Since each company creates a slightly different firmware, there is a lot of variation in how to interrupt the normal startup, so this step might take some experimentation.

### Interrupt startup

With your system *fully* shutdown (not hibernated or suspended), plug your USB drive into your computer. 

Press the power button--then watch closely!

Each device is different, but just as the computer starts to boot you should see a screen with the manufacture’s logo and a message that tells you which key to press to "interrupt the boot process", enter BIOS/UEFI, or "choose a boot device".
It often flashes by so fast you can’t read it! 

The interrupt key is usually Delete, Esc, F12, F11, F10, F9, F1, or F2
(check some tips from [Pendrivelinux](https://www.pendrivelinux.com/how-to-access-bios/) or [gpost](https://www.groovypost.com/howto/bios-uefi-setup-guide-boot-from-cd-dvd-usb-drive-sd-card/)).
If your laptop has a compact keyboard, you may need to use a key combo (`fn` + number key).
Click the key repeatedly until you get a response, if it flashes by too quick and starts booting Windows, hold down the power button to shut down, then try again.

On older Macs, immediately press and hold the `Option` key. 
This should bring you to the "Startup Manager" allowing you to select the USB drive (more tips on [Mac help](https://support.apple.com/en-us/HT202796)).

If your system already had Linux installed, if you get to the GRUB boot menu, use arrow keys to select "System Setup". This should open the machine's BIOS/UEFI menu, which will have a boot device option.

### Choose boot device

Once you interrupt the startup process you need to tell the system to boot using the USB drive rather than the default hard drive. 
Here are the mostly likely options you will see:

- **Choose Boot Device:** If you are lucky, your vendor provides the "choose a boot device" option. Once you click the correct key, a small menu will appear listing the available disk drives in the system. Look for your USB's label and size to identify the correct drive. Use the arrow keys to highlight the USB drive, then click enter to boot.
- **BIOS Boot Order:** For older systems if you get into a BIOS menu, but can't find a "choose a boot device" option, look for a "Boot order" setting. Use the menu to change the boot order, moving USB drives to the top (traditionally, optical drives are at the top, then hard drives). Save and exit the BIOS menu and reboot--the USB should boot automatically.
- **Locked down UEFI:** On some Windows 10 / 8 machines, UEFI has been made a bit more complicated and there is no boot device or boot order options at start up. Allow Windows to boot up. First, make sure you have disabled "Fast Startup" as described below. Then, go to the Windows shutdown menu, hold the `shift` key and click Restart. This should bring up a blue boot options menu, select "Use a device", then select your USB.  Alternatively, try Settings > Update & security > Recovery, then look for "Advanced startup" and click "Restart now".

There is a lot of variation in exactly how to access BIOS and UEFI options from different computer companies, so if none of this seems to work, try searching for help using your specific model and manufacturer. 

Hopefully, you have finally got your system to boot from the live USB--now you should see a menu provided by your distro's installer offering options like "Try Ubuntu without installing" and "Install Ubuntu". 
Choose the "Try" option.
Your live session will boot from the USB (without changing your main hard drive).

{% include card.html header="Windows 10 / 8 Fast Startup" text='
Windows overwrites parts of the file system to enable quicker boot times, bypassing the traditional boot process. 
This "Fast Startup" generally needs to be disabled or you will not have the option to boot from USB and your linux install will not be able to properly identify the Windows boot manager.

With Windows running: 

- Open the Control Panel > Power Options.
- Click "Choose what the power button does", then "Change settings that are currently unavailable"
- Uncheck the box next to "Turn on fast startup (Recommended)"
- Completely shutdown your computer (not sleep, hibernate, or restart).
' %}

{% include card.html header="Secure Boot" text='
Newer PCs have a [Secure Boot](https://en.wikipedia.org/wiki/Unified_Extensible_Firmware_Interface#Secure_boot) feature that prevents unsigned OS from booting on the system.
Major distributions (Ubuntu, Fedora, SUSE) have secure signatures that allow them to run on systems with Secure Boot (you do NOT need to disable it).
However, smaller distros do not, so the Secure Boot may need to be disabled.

If you try the booting from USB, but after selecting the drive the system skips it and boots into the normal OS--Secure Boot is probably at work and should be disabled.

To disable Secure Boot: 

- Enter your BIOS menu during boot (see tips as below) or while in Windows: go to the shutdown menu, hold the `shift` key and click Restart, from the recovery menu select "Troubleshoot" then "Advanced Options: UEFI Firmware Settings".
- Look for the Secure Boot settings under the Security, Boot, or Authentication tab (each manufacturer is different).
- Set Secure Boot to Disabled.
- Save changes and exit

(See more advice from [Microsoft help](https://docs.microsoft.com/en-us/windows-hardware/manufacture/desktop/disabling-secure-boot))
' %}

{% capture virtual %}
Using a live USB provides the best testing experience, letting you see how the distro works on real hardware.
However, there are some other options:

- [Distrotest](https://distrotest.net/index.php) will boot up a virtual machine with your distro of choice and open a remote desktop window right in your browser. The performance is slow (depending on your connection and the VM) and not exactly like using real hardware, but can be a nice option to quickly check out a new OS.
- [VirtualBox](https://www.virtualbox.org/wiki/Downloads) or other virtualization software can be used to test any distro in a disposable virtual machine. The performance will be limited, but it is an easy way to test something out or see what the install process looks like--and grab screenshots for tutorials or debugging.
{% endcapture %}
{% include card.html text=virtual header="Virtual Test Drive" %}
