---
title: Getting Started with Your Distro
nav: Use
topics: Installing tips; Linux basics
---

With your distro's live session booted from USB, you can now explore Linux!

Performance in the live session is generally not as good as an actual install, but it should give you an idea of how well it works with your particular hardware.
Advanced drivers for your CPU, video card, or other specialized features will not be loaded--everything should work, but maybe not as good as it will with a full install.

You can click around the live session to see how everything works. 
Open applications, switch workspaces, connect to the internet, and browse the software center--get a feel for what the distro offers.

The live session will have an app to permanently install the OS on your machine.
Most installers are graphical and user-friendly, and will guide you through the process--generally there is just a few button clicks and a lot of waiting around!
Check out Ubuntu's official [install tutorial](https://tutorials.ubuntu.com/tutorial/tutorial-install-ubuntu-desktop) to get a sense of what it looks like.

{% capture basics %}
## Linux Basics

If you have ever used a computer, almost everything will be familiar! 
No big deal.
Here are a few things slightly different from Windows:

- **User accounts and passwords** - You are always logged in as a user and require a password to make any changes to the system (Windows tends to hide this).
- **File system, home directory** - Linux uses a file system that Windows can't read and is presented differently. On Windows the root is the drive letter `C:\`. Linux presents all drives as a unified file system, with the root at `/` and your user directory at `/home/username` (Linux doesn't use Windows back slashes `\`).
- **Updates** - Updates are pushed out regularly keeping you secure and fixing bugs--updates are *much* more common than on Windows, yet usually less of a hassle. The updates cover the OS *and* all applications installed from a repository. First, the catalog of all software in the distro's repositories is updated, then updates that apply to your installed software (and dependencies) are downloaded. There is usually an updater application, but you may need to start it manually.
- **Software center** - Applications can be easily and securely installed from your distro's repository. There is usually an GUI app to find and manage software curated by the distro. Recently distro independent application packaging frameworks are supplementing or replacing traditional software repositories. The main frameworks include Snap (Ubuntu, [Snapcraft](https://snapcraft.io/)), Flatpack ([Flathub](https://flathub.org/)), and [Appimage](https://appimage.org/). These formats simplify software distribution, as each package has all dependencies fully self-contained (and often sandboxed).
- **Terminal** - Command line is really handy! See this [mini-workshop](https://evanwill.github.io/_drafts/notes/commandline.html).

{% endcapture %}
{% include card.html text=basics %}
