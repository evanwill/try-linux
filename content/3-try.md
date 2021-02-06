---
title: How to Test A Distro
nav: Try
topics: Burn ISO; Boot live USB
---

## Try 

The best way to learn Linux is to try it.

When you buy a Windows, Chromebook, or Mac computer, the operating system (OS) comes pre-installed. 
However, if you are interested in running Linux or other open OS, you will usually have to install it yourself.

Most modern Linux distros are released as an ISO disk image, usually a "live cd" or "live usb".
This means you can download an ISO, burn it to a USB stick, and then boot up into the live desktop without actually installing or changing your hard drive!

Give it a try with these instructions to [burn an ISO](https://evanwill.github.io/_drafts/notes/burn-iso.html) and [boot a live USB](https://evanwill.github.io/_drafts/notes/linux-boot-usb.html).

Once you try it out, install it!

> Alternatively, if you *really* don't want to even download anything, you can visit [Distrotest](https://distrotest.net/index.php).
> Distrotest will boot up a virtual machine with your disto of choice and open a remote desktop window right in your browser.
> The performance is slow (depending on your connection and the VM) and not exactly like using real hardware, but can be a nice option to quickly check out a new OS.
> 
> As another option, you can install [VirtualBox](https://www.virtualbox.org/wiki/Downloads) on a computer to try out any distro in a disposable virtual machine.
> The performance will be very limited, but it is an easy way to test something out or see what the install process looks like--and grab screenshots for tutorials or debugging.
>
> Manufactures such as Dell and Lenovo are offering more computers with Linux pre-installed, and Linux specific companies such as [System76](https://system76.com/) are booming. 
> More manufactures offering devices means better hardware support is being built into the Linux kernel.

------

## Background

Burning a disk image or bootable USB stick is an important task if you want to use Raspberry Pi or Linux. 
When you buy a Windows, Chromebook, or Mac computer, the operating system (OS) comes pre-installed. 
However, if you are interested in running Linux or other open OS, you will most likely have to install it yourself. 
Traditionally, installation was done by burning a disk image onto a CD or DVD. 
Since most devices no longer have optical drives, we now create bootable SD or USB instead. 

## Copying files versus burning an image

A Raspberry Pi doesn't come with an OS. 
To get started using your Pi, you need to add a OS to a SD card. 
You can simply copy [NOOBS](https://www.raspberrypi.org/downloads/noobs/) on to an SD card, and it will magically work! 
But that is **NOT** burning a disk image. You have only copied the files on to the SD's existing file system.

If you want to try any other Pi OS, it will come as an IMG file.
Most [linux distributions](https://distrowatch.com/) are provided as an ISO file.
IMG and ISO are exact binary copies of a storage device. 
If you simply copy them over to an SD, nothing will happen. 
The image has to be "burnt", essentially overwriting the entire media removing the existing file system.

So let's get an image and burn it to some media!

## 1. Get an IMG / ISO

For Raspberry Pi and other single board computers, you will usually get an IMG file representing an hard drive image. 
These are often zipped or in some other archive (`.zip` or `.xz`) to decrease the download size. It is not necessary to unzip. 
For example:

- [Raspbian](https://www.raspberrypi.org/downloads/raspbian/) Official OS of Raspberry Pi
- [Volumio](https://volumio.org/)

Linux distros are generally released as an ISO, often called a "live cd" or "live usb" meaning it can boot from the install media.
For example:

- [Ubuntu](https://www.ubuntu.com/)
- [KDE Neon](https://neon.kde.org/)

Some linux distros are specifically designed to be portable. 
You always use them from a USB stick and do not install to a hard drive.
For example: 

- [Puppy Linux](http://puppylinux.org/)
- [Slax](https://www.slax.org/en/)
- [Porteus](http://www.porteus.org/)

Many specialized utilities are also distributed as images so that they can be run from portable media to make changes to a system without a functioning OS. 
For example:

- [GParted Live](https://gparted.sourceforge.io/livecd.php)
- [DBAN](https://dban.org/)
- Anti-virus rescue CDs
	- [Bitdefender](https://www.bitdefender.com/support/how-to-create-a-bitdefender-rescue-cd-627.html)
	- [AVG](http://www.avg.com/gb-en/rescue-cd-business-edition)

## 2. Get media

Now you need a micro SD card for Raspberry Pi or a USB stick for linux on a computer.
Be sure to get media that is bigger than the image you want to burn! 

- **SD cards:** There is a confusing variety of SD cards out there today. Look for one labelled SDHC (SDXC are incompatible with some systems), Class 10 / UHS 3. The numbers aren't essential, but faster read/write speeds will give better performance. 8GB is standard, but I like to get at least 16GB, since the SD card will be the main hard drive for your Pi. If your computer does not have an SD slot, get a SD reader.
- **USB drives:** Most USB drives will be fine for installing linux. However, if you want to use it as a live USB or portable desktop, look for USB 3 versions with faster read/write speeds if possible.

> **Optional: Format media.**
> If you have previously used the media, you might want to start with a nice clean disk by re-formatting. 
> If you are on Windows or Mac, get the official [SD Formatter](https://www.sdcard.org/downloads/formatter_4/index.html).
> This will enable you to restore SD or USB you have previously burnt, which Windows and Mac are unable to actually read. 
> On linux, the built in formatting utilities are generally sufficient to restore and format media. If necessary use Gparted and format to fat32.
> However, when using Etcher, formatting before burning is rarely necessary.

## 3. Get Etcher

[Download Etcher](https://www.balena.io/etcher/) for your system, and extract the `.zip` file (you should get a single `.AppImage` file on Linux or an `.exe` on windows).

Why Etcher and not the million other options out there? 

- Easy to use, it automatically selects the right drives and just works!
- Can burn from archived (.zip, .7z, etc) images automatically.
- Open source, cross platform, and easy to install.
- New and actively developed (most are not).
- Fast and efficient, with built in verification of the burn.

## 4. Burn image

Start up Etcher by clicking on the `.AppImage` or `.exe` file. Etcher makes the rest easy!

1. Plug your media into the computer.
2. Select the image.
3. Select the SD/USB (if you have only one plugged in, it will be automatically selected).
4. Click Flash! (you may need to authenticate at this point, since you are making changes to a drive)
5. Wait. Wait... 
6. Remove your SD/USB.

Now you can go play with your Raspberry Pi or try out a new Linux distro!

Next, see [Boot a Live USB](https://evanwill.github.io/_drafts/notes/linux-boot-usb.html) for tips about how to get the USB to boot on your computer.



------

Burning a live USB is a great way to test out Linux distros (*see* [Burn SD/USB](https://evanwill.github.io/_drafts/notes/burn-iso.html) and [Linux Intro](https://evanwill.github.io/_drafts/notes/linux-intro.html) notes). 
However, for it to work you need to boot from USB. 
For most systems this is not the default and you will have to intervene as your computer starts up.

The boot process is controlled by the BIOS or UEFI installed by your computer manufacturer. 
Since each company creates a slightly different firmware, there is a lot of variation in how to exactly interrupt normal startup--but this note tries to gather some general tips together. 

## Backup

If you are messing around with your computer, its a good time to take some basic precautions to give you peace of mind--these are best practices that you should follow anyway!
Backup of all your files on external storage to make sure you have everything you *really* want saved in multiple stable locations.

On Mac, review how to get to [macOS Recovery](https://support.apple.com/en-us/HT201314).
On Windows, make a Windows Recovery Drive on a USB stick (search your system for "recovery" and the option to create a recovery drive will pop up. This ensures you can reinstall or repair Windows if necessary).

## Windows 10 / 8 Prep

Windows 10 / 8 overwrite parts of the file system to enable quicker boot times, bypassing the traditional boot process. 
This "Fast Startup" needs to be disabled or you will not have the option to boot from USB and your linux install will not be able to properly identify the Windows boot manager.

- Open the Control Panel > Power Options.
- Click "Choose what the power button does", then "Change settings that are currently unavailable"
- Uncheck the box next to "Turn on fast startup (Recommended)"
- Completely shutdown your computer (not sleep, hibernate, or restart).

## Secure Boot

Newer PCs have a [Secure Boot](https://en.wikipedia.org/wiki/Unified_Extensible_Firmware_Interface#Secure_boot) feature that prevents unsigned OS from booting on the system.
Major Linux distributions (Ubuntu, Fedora, SUSE) have secure signatures that allow them to run on systems with Secure Boot (you do NOT need to disable it).
However, smaller distros do not, so the Secure Boot will have to be disabled.
If you try the Boot USB tips below, but after selecting the USB the system skips it and boots into the normal OS--Secure Boot is probably at work and should be disabled.

To disable Secure Boot: 

- Enter your BIOS menu during bootup (see tips as below) or while in Windows: go to the shutdown menu, hold the `shift` key and click Restart, from the recovery menu select "Troubleshoot" then "Advanced Options: UEFI Firmware Settings".
- Look for the Secure Boot settings under the Security, Boot, or Authentication tab (each manufacturer is different).
- Set Secure Boot to Disabled.
- Save changes and exit

(See more advice from [Microsoft help](https://docs.microsoft.com/en-us/windows-hardware/manufacture/desktop/disabling-secure-boot))

## Boot USB

With your system fully shutdown, plug your Live USB into your computer. 

If your computer currently has Linux or Mac installed, it *might* be easy:

- **On Linux:** turn on the computer, when you see the GRUB boot menu, use arrow keys to select "System Setup". This should open the machine's BIOS/UEFI menu, which should have a boot device option.
- **On Mac:** turn on the computer, immediately press and hold the `Option` key. This should bring you to the "Startup Manager" allowing you to select the USB drive (more tips on [Mac help](https://support.apple.com/en-us/HT202796)).

*Otherwise*, try the following tips:

Press the power button--then watch closely! 
Each device is different, but just as the computer starts to boot you should see a screen with the manufacture’s logo and a message that tells you which key to press to "interrupt the boot process", enter BIOS/UEFI, or "choose a boot device".
Sometimes it flashes by so fast you can’t read it! 

The key is usually F12, Esc, F11, F10, F9, F1, F2, or DEL (here are some tips from [Pendrivelinux](https://www.pendrivelinux.com/how-to-access-bios/) or [gpost](https://www.groovypost.com/howto/bios-uefi-setup-guide-boot-from-cd-dvd-usb-drive-sd-card/)).
If your laptop has a compact keyboard, be sure to use the correct key combo (often `fn` + key).
Click the key repeatedly until you get a response, if it flashes by too quick and starts booting Windows, hold the power button to shut down, then try again.

Here are some possible outcomes: 

- **Choose Boot Device:** If you are lucky, your vender provides the "choose a boot device" option. Once you click the correct key, a small menu will appear listing the available disk drives in the system. Look for your USB's label and size to identify the correct drive. Use the arrow keys to highlight the USB drive, then click enter to boot--Success!
- **BIOS Boot Order:** For older systems if you get into a BIOS menu, but can't find a "choose a boot device" option, look for a "Boot order" setting. Use the menu to change the boot order, moving USB drives to the top (traditionally, optical drives are at the top, then hard drives). Save and exit the BIOS menu and reboot--the USB should boot.
- **Locked down UEFI:** On some Windows 10 / 8 machines, UEFI has been made a bit more complicated and there is no boot device or boot order options at start up. Allow Windows to boot up. First, make sure you have disabled "Fast Startup" as described above. Then, go to the Windows shutdown menu, hold the `shift` key and click Restart. This should bring up a blue boot options menu, select "Use a device", then select your USB.  Alternatively, try Settings > Update & security > Recovery, then look for "Advanced startup" and click "Restart now".

There is a lot of variation in exactly how to access BIOS and UEFI options from different computer companies, so if none of this seems to work, try searching for help on your specific model and manufacturer. 
