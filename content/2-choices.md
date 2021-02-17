---
title: Choose a Distribution
nav: Distro
topics: What is a Distro? How do you choose one?
description: To get started you will need to choose a distro to try. This section presents info to demystify the options.
---

When you buy a Windows, Chromebook, or Mac computer, the OS comes pre-installed. 
However, if you are interested in running Linux you will usually have to install it yourself.
The first step is to choose *which* Linux you want to try!

Linux OS are usually shipped as a complete package of components called a <span class="term">Distribution</span>, or "distro".
They include the low-level technical stuff, plus a desktop environment and selection of basic applications.
There are hundreds of distros to choose from, maintained by independent organizations, communities, or individuals, each with different philosophies, strengths, and use cases.

Surf <span class="term">[Distrowatch](https://distrowatch.com/)</span> to browse the latest news and reviews.

{% include alert.html color="success" text="If you just want a quick suggestion of a distro to try, choose [Ubuntu Desktop](https://ubuntu.com/download/desktop) or an [Ubuntu flavor](https://ubuntu.com/download/flavours). Ubuntu is the most popular desktop Linux and has plenty of help readily available." %}

-------------

## Choosing a Distro

Part of the fun of getting started with Linux is choosing a distro, but there are so many that it can also be overwhelming.

Browse the [Major Distro Families]({{ '/content/5-resources.html#major-distro-families' | relative_url }}) in Resources and consider some of these aspects:

{% capture consider %}
### Community and Philosophy

Do you want to search online and find hundreds of answers to your questions (Ubuntu), be part of a values driven community (Fedora), or get involved in a smaller forum of deeply invested enthusiasts (Arch)? 
Do you want everything to just work (Ubuntu) or are you willing to spend time customizing (Arch)?

The community and philosophy of a distro impact the out-of-the-box experience and how much help is available.

In general, Ubuntu has the largest user community, so if you search for help the majority of answers directly relate to Ubuntu.
However, other communities have very active forums, wikis, and documentation to get people involved.
If you use a Linux server at work or in another project, choosing a distro from the same family will make life easier and increase your familiarity.

----------

### Repositories and Software

Distros offer a <span class="term">repository</span> used manage and update pre-packaged software prepared for the OS.
This includes required low-level stuff as well as desktop applications for users.

Some distros have huge repos of vetted stable applications (Debian),
others are more up to date (Fedora), 
or contain more community packages (Arch).
Some distros package only free software that meets their community guidelines (Fedora), while others include commonly used (but non-free software) such as MP3 or DVD encodings (Ubuntu).

----------

### Release Type

Do you want to install a stable OS that will be supported for a *LONG* time so that you won't have to upgrade or do you always want the latest-and-greatest?

Distros typically follow either a rolling or fixed release schedule. 

<span class="term">Rolling release</span> distros have a continuous stream of updates, you always have the latest software and never have to upgrade to a new version (but may encounter some instability). 

<span class="term">Fixed release</span> are more traditional and stable with incremental versions that may require a large upgrade every so often. 
Fixed releases are often broken into latest and LTS (long term support)--if you want to install once, and use the system for years without needing to upgrade, choose an LTS. 
For example, Ubuntu normal releases are officially supported for nine months and LTS for five years.

----------

## Hardware

One of Linux's strengths is flexibility to run on any hardware, from Raspberry Pi to the fastest super computers.
Likewise, it will run on pretty much any desktop or laptop computer you might have, with support baked directly into the Kernel.

However, you will get the best experience if you find a distro suited to your hardware:

- If you have an old computer bogged down by Windows, there are many "light" distros designed to revive it.
- If you have brand new laptop, look for distros with the most up to date kernel for full support of advanced features and performance. 
- If you have an advanced graphics card, try to look for distros that specifically support it.

----------

### Installer Options

In the past Linux distros were confusing to install, forming a major barrier to adoption.
Ubuntu really changed that, and some installers are still friendlier than others. 

- <span class="term">Secure Boot UEFI</span> - If you have a newer computer, it will have Secure Boot UEFI which is only supported by the bigger Linux distros (Ubuntu, Fedora, SUSE)--otherwise you will have to tweak your UEFI / BIOS to get the installer to work.
- <span class="term">Dual booting</span> - Do you want to keep windows? Some installers make it easy (Ubuntu).
- <span class="term">Disk encryption</span> - Some distros now support full encryption for your hard drive as an option during install. In most set ups this will require a separate password, so during boot you unlock the encryption, then log into the system.

{% endcapture %}
{% include card.html text=consider %}

-------------------

## Desktop Environment

Unlike windows, mac, or chrome, Linux desktops are separate from the core and can be installed independently.
So after choosing a distro, you will also usually have a choice of <span class="term">desktop environment</span> (DE)--the graphical interface you will be staring at all day!

Generally, you will choose a package pre-bundled with a DE, most distros will give you several options, with <span class="term">GNOME</span>, <span class="term">KDE</span>, and <span class="term">Xfce</span> being most common.
Distros often tweak their versions of the desktops, so the final look, default software, and features vary a bit. 
Just take a look at their screenshots and decide! 

Things to consider:

- Weight - How resource intensive is it? Slicker desktops (GNOME, KDE) require modern hardware to run well. If you have an old computer or low spec hardware, go light (Xfce, LXqt)!
- Configurability - How much do you want to tweak the look and feel? Do you want it to just look good out of the box?
- Unique vs. traditional - Do you want something different (GNOME) or are you nostalgic for the old days (Cinnamon)?

See [Major Desktop Environments]({{ '/content/5-resources.html#major-desktop-environments' | relative_url }}) in Resources for more details.

{% include alert.html color="info" text="Manufactures such as Dell and Lenovo are offering more computers with Linux pre-installed, and Linux specific companies such as [System76](https://system76.com/) are booming. More manufactures offering devices means better hardware support is being built into the Linux kernel, which is great for everyone!" %}
