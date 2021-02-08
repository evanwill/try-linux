---
title: Introduction to Linux
nav: Intro
topics: What is Linux? Why Linux?
---

## What is Linux?

<span class="term">Linux</span> is a family of open source operating systems (OS) used to run all kinds of computers, from laptops to super computers.
You might hear "Unix-like" or "*nix", since Linux is part of a group of OS descended from the early research computing system [UNIX](https://en.wikipedia.org/wiki/Unix).

<div class="border rounded px-3 py-2 mb-3 text-center">
<audio controls class="w-100">
    <source src="https://upload.wikimedia.org/wikipedia/commons/0/03/Linus-linux.ogg" type="audio/ogg">
    Your browser does not support the audio element.
</audio>
<small>"Hello! This is Linus Torvalds, and I pronounce Linux as /ˈlinʊks/." (<a href="https://commons.wikimedia.org/wiki/File:Linus-linux.ogg">Wikimedia Commons</a>)</small>
</div>

An <span class="term">OS</span> is made up of a many components, basically:

- **Bootloader:** starts the low level processes necessary to boot an OS, most linux distributions use [GRUB](https://www.gnu.org/software/grub/).
- **Kernel:** manages the hardware and low level software components, coordinating the complete OS. This is actually "[Linux](https://www.kernel.org/)".
- **Shell:** text-based command line interface.
- **Desktop environment:** graphical interface.
- **Applications:** individual programs run from the desktop or shell.

The core of Linux, <span class="term">[The Kernel](https://www.kernel.org/)</span>, is developed by the [Linux Foundation](https://www.linuxfoundation.org/about/) and original creator Linus Torvalds, with contributions from thousands of people and corporations around the world.
Linux operating systems are usually shipped as a complete package of components called a <span class="term">distribution</span>, or "distro".
There are hundreds of distros to choose from, maintained by independent organizations, communities, or individuals, each with different philosophies, strengths, and use cases.

## Why Linux?

Linux core is <span class="term">[Free Software](https://www.gnu.org/philosophy/free-sw.en.html)</span>, meaning cost-free and freely licensed.

{% include video-embed.html youtubeid="n9D7oeM3zd8" caption="Freeeeeeeeeeeedoooooooooom!" %}

<span class="term">This gives you freedom: you can fully control, inspect, modify, copy, and share the OS.</span>

But for most users, that is not necessarily the most compelling reason to use Linux. 
Instead they just appreciate a solid, powerful, and user-friendly OS.
Linux provides performance, security, privacy, and cost benefits, in addition to access to a huge ecosystem of open-source applications and services.

Linux runs the vast majority of web servers (95%+), super computers (all of the top 500), smart phones (80%+), Chromebooks, IoT, and single board computers. 
So if you want to use a VM in the cloud, do high performance computing, or tinker with a Raspberry Pi at home, it's helpful to know Linux.

But it also makes a great desktop OS for your personal computer!
Thus, there are many practical *and* ideological reasons to use Free and Open software.

For an in depth introduction, try the free course from the Linux Foundation, [Introduction to Linux](https://training.linuxfoundation.org/training/introduction-to-linux/).

{% include alert.html color="secondary" text="### Bloatware, adware, viruses, oh my!

Many people are sick of the shady commercial practices of Windows, Apple, and PC manufacturers that put user security and privacy at risk.
Proprietary OS limit your rights and control as a user.
Linux distros are viable alternatives!" %}
