---
title: Resources
nav: Resources
---

# Major Desktop Environments

The major desktops can be divided by their "widget toolkit" used to create the GUI elements and default applications.
This is probably the last time you will ever hear "widget toolkit", but you might hear something like GTX theme or Qt application.
The details aren't important, but you will see some family resemblance.
All desktops can support both GTX and Qt applications, but software in the native toolkit will have more closely integrated and themed.

Major desktops:

- [GTX based](https://en.wikipedia.org/wiki/GTK)
    - [GNOME](https://www.gnome.org/). modern, minimalist-style, unique "Activities Overview" (no start menu), [extensions](https://extensions.gnome.org/) add functionality, and themes easily change the look.
    - [Xfce](https://www.xfce.org/). lighter weight, simple, stable, traditional linux desktop. Offered as the default of many distros, often highly customized.
    - Less common:
        - [Cinnamon](http://developer.linuxmint.com/projects.html). more traditional desktop with start menu (get newest version with [Mint](https://www.linuxmint.com/)).
        - [Budgie](https://budgie-desktop.org/). slick, GNOME-based (get newest version with [Solus](https://getsol.us/home/)).
        - Pantheon. polished, GNOME-based (developed by [ElementaryOS](https://elementary.io/))
        - [MATE](https://mate-desktop.org/). traditional, lighter weight, based on an old version of GNOME.
        - [LXDE](http://lxde.org/). very light weight, basic features (development has shifted to LXQt instead, so check out LXQt instead). 
        - Historic note: ~~Unity~~. Until version 17.10, Ubuntu shipped with a unique desktop. However, Ubuntu's GNOME theme emulates the Unity look.
- [Qt based](https://en.wikipedia.org/wiki/Qt_(software))
    - [KDE](https://www.kde.org/). very configurable, complex, windows-like (get newest version with [Neon](https://neon.kde.org/)).
    - [LXQt](http://lxqt.org/). very light weight, basic features (sibling of LXDE).
    - DDE. Polished desktop of [Deepin linux](https://www.deepin.org/en/) (Chinese focused), recently becoming available in other distros.
- Other
    - Tiling window managers (the traditional desktop metaphor is replaced by automatically dividing the screen with your open application windows, controlled by key commands, for a simple and efficient desktop. There is a bit of a learning curve!) Checkout [xmonad](http://xmonad.org/) or [i3](https://i3wm.org/). For any easy intro, checkout [Regolith Linux](https://regolith-linux.org/) which combines i3-wm with Ubuntu.

> Most desktops support themes which make it easy to change the look and feel. 
> For example check out the themes page at [OMG! Ubuntu!](http://www.omgubuntu.co.uk/category/themes-2).

# Major Distro Families

Below is a basic introduction to the major linux families, with a focus on distros with desktop friendly versions.

### Debian

One of the oldest active linux distros, Debian has extensive stable repositories that are the base of MANY other distros. 
This includes Ubuntu, developed by enterprise software company [Canonical](https://www.canonical.com/) based in the UK.
Uses `apt` configuration and `.deb` packages.

- [Debian](https://www.debian.org/), entirely free software released by the Debian Project. [Debian packages](https://www.debian.org/distrib/packages).
- [Ubuntu](https://www.ubuntu.com/), the most popular desktop linux, beginner friendly. [Ubuntu Packages](https://packages.ubuntu.com/) and [Snapcraft](https://snapcraft.io/).
    - [Ubuntu flavors](https://ubuntu.com/download/flavours), Ubuntu spins featuring alternative desktops.
    - [Linux Mint](https://www.linuxmint.com/), one of the most popular and beginner friendly, featuring the Cinnamon desktop.
    - [Elementary OS](https://elementary.io/), stylish mac replacement, unique Pantheon desktop.
    - [Pop!_os](https://system76.com/pop), customized Gnome desktop with some unique addons, built by computer company [System76](https://system76.com) focused on developers.
    - [KDE Neon](https://neon.kde.org/), cutting edge KDE on Ubuntu base.
    - [Zorin OS](https://zorinos.com/), polished windows replacement.
    - [Linux Lite](https://www.linuxliteos.com/), focused on easy to use, windows replacement, with Xfce.
    - [Bodhi Linux](https://www.bodhilinux.com/), minimalist, lightweight distro with unique Moksha desktop.
    - [Peppermint](https://peppermintos.com/), ChromeOS-like cloud focused minimal desktop.
    - [GalliumOS](https://galliumos.org/), Xubuntu based replacement for Chromebook hardware.
- [Raspbian](https://www.raspberrypi.org/downloads/raspbian/), Official OS of Raspberry Pi, unique Pixel desktop.
- [Endless OS](https://endlessos.com/home/), simplified, education focused system designed for offline use, by computer company [Endless](https://endlessos.com/computers/).
- [deepin](https://deepin.org/), Chinese based distro with unique desktop and apps. 

### Fedora / RedHat

Based in the USA, [Red Hat](https://www.redhat.com/) is one of the largest open-source enterprise software companies, providing support, development, and Linux OS to major corporations.
It is a good choice to learn if you are interested in working with enterprise environments.
Uses `yum` or `dnf` configuration and `.rpm` packages.

- [Fedora](https://getfedora.org/), open project sponsored by Red Hat with a focus on free-software. Considered fairly cutting edge with two new versions each year, a testing ground for RHEL, yet stable enough for most users. [Fedora Packages](https://apps.fedoraproject.org/packages/).
    - [Fedora Spins](https://spins.fedoraproject.org/), alternative desktops.
    - [Fedora Labs](https://labs.fedoraproject.org/), specialized distros from science to music.
    - [Sugar on a Stick](https://spins.fedoraproject.org/en/soas/), very unique kid focused learning platform, packaged to run on a live USB. Learn more at [Sugar Labs](https://www.sugarlabs.org/).
- [Red Hat Enterprise Linux (RHEL)](https://www.redhat.com/en/technologies/linux-platforms/enterprise-linux), an industry standard, non-free.
- ~~[CentOS](https://www.centos.org/)~~, free community supported RHEL. Once very popular, was unexpectedly discontinued in 2020 during Red Hat corporate changes.
- ~~[Scientific Linux](https://www.scientificlinux.org/)~~, free RHEL-based OS developed by Fermilab for high performance scientific computing environments (is now being phased out in favor of CentOS).

### SUSE

Germany based enterprise FOSS company.
Uses `ZYpp` or `YaST` for configuration and `.rpm` packages.

- [openSUSE](https://www.opensuse.org/), developer focused with a rolling release option, Tumbleweed. *Note: openSUSE default install ISO are not live images and can not be used to try without installing. They provide a separate live image, but it is not complete and cannot be used to install.* [openSUSE Packages](https://software.opensuse.org/find).
    - [GeckoLinux](https://geckolinux.github.io/), openSUSE spin focused on being user friendly.
- [SUSE Linux Enterprise](https://www.suse.com/), commercial distro with focus on mature and stable server environments.

### Arch

An independent, community built family with rolling release following a *K.I.S.S.* and DIY philosophy. 
Not traditionally user friendly.
Uses `pacman` for configuration. [Archlinux packages](https://www.archlinux.org/packages/).

- [Arch](https://www.archlinux.org/)
- [Manjaro](https://manjaro.org/), user friendly Arch for beginners.
- [EndeavourOS](https://endeavouros.com/), intended to build user-friendly installer and community for Arch.

### Others

**Independent.** Some distros go it alone. For example:

- [Solus](https://getsol.us/home/), up-and-coming independent distro developing Budgie desktop.
- [Qubes OS](https://www.qubes-os.org/), personal security focused distro with unique architecture that isolates all software in separate VM-like containers. Major distros have also started offering fully containerized OS versions for max security and stability, such as [Ubuntu Core](https://ubuntu.com/core) and [Fedora Silverblue](https://silverblue.fedoraproject.org/) (see [explainer article](https://arstechnica.com/gadgets/2021/02/ubuntu-core-20-adds-secure-boot-with-hardware-backed-encryption/)).
- [Alpine Linux](https://www.alpinelinux.org/), minimalistic, security focused distro from Norway, commonly used as basic server image or as base for containers.
- [Linux From Scratch](http://www.linuxfromscratch.org/), build everything yourself, step-by-step DIY!

**Portable.** Some linux distros are specifically designed to be portable, i.e. you always use them from a USB stick and do not install to a hard drive.
This makes them simple, fast, and secure.
For example:

- [Puppy Linux](http://puppylinux.org/)
- [Slax](https://www.slax.org/en/)
- [Porteus](http://www.porteus.org/)

**Android.** Based on Linux, Android is the most popular smart phone OS in the world.

- [Android-x86](http://www.android-x86.org/), port of Android that can be run on a laptop.

**Entertainment.** There are many specialized minimalist distros that act as entertainment centers, usually run on a Raspberry Pi or similar device.

- music player: [Volumio](https://volumio.org/).
- media center: [OSMC](https://osmc.tv/) or [OpenELEC](http://openelec.tv/).
- gaming: [RetroPie](https://retropie.org.uk/) or [SteamOS](http://store.steampowered.com/steamos/).
- NAS: [FreeNAS](http://www.freenas.org/) or [EasyNAS](http://www.easynas.org/). 

**Utilities.** Some specialized distros are basic utilities used to work on a computer where the main drive or OS maybe corrupted.

- [GParted Live](https://gparted.sourceforge.io/livecd.php), partition and disk utility.
- [Clonezilla](http://www.clonezilla.org/), disk imaging/cloning deployment or recovery.
- [DBAN](https://dban.org/), disk data destroyer.

### Other open OS 

There are other open-source OS out there, Linux is just the most popular.

- BSD: a family of OS descended from [Berkeley Software Distribution](https://en.wikipedia.org/wiki/Berkeley_Software_Distribution) Unix. Considered rock-solid stable and secure for servers, with desktop options [FreeBSD](https://www.freebsd.org/) and [TrueOS](https://www.trueos.org/).
- OpenSolaris / illumos / SunOS: a family of Unix-like OS descended from proprietary enterprise systems, currently openly developed by the [openindiana](https://www.openindiana.org/) community.
- [Haiku](https://www.haiku-os.org/), based on BeOS, an early competitor to Mac.
- [KolibriOS](http://kolibrios.org/en/), minimalist, tiny OS.
- [Redox OS](https://www.redox-os.org/), newly developed OS written in [Rust](https://www.rust-lang.org/en-US/) language.

# Common Applications


# Resources
