---
title: Getting Started with Your Distro
nav: Use
topics: Installing tips; Linux basics
---


The live session will have an app to permanently install the OS on your machine.
Most installers are graphical and user-friendly.
Here is Ubuntu's official [install tutorial](https://tutorials.ubuntu.com/tutorial/tutorial-install-ubuntu-desktop).


## Basics

If you have ever used a computer, almost everything will be familiar! No big deal.
Here are a few things slightly different from Windows:

- **User accounts and passwords.** You are always logged in as a user and require a password to make any changes to the system (Windows tends to hide this).
- **File system, home directory.** Linux uses a file system that Windows can't read and is presented differently. On Windows the root is the drive letter `C:\`. Linux presents all drives as a unified file system, with the root at `/` and your user directory at `/home/username` (Linux doesn't use Windows back slashes `\`).
- **Updates.** Updates are pushed out regularly keeping you secure and fixing bugs--updates are *much* more common than on Windows, yet usually less of a hassle. The updates cover the OS *and* all applications installed from a repository. First, the catalog of all software in the distro's repositories is updated, then updates that apply to your installed software (and dependencies) are downloaded. There is usually an updater application, but you may need to start it manually.
- **Software center.** Applications can be easily and securely installed from your distro's repository. There is usually an GUI app to find and manage software curated by the distro. Recently distro independent application packaging frameworks are supplementing or replacing traditional software repositories. The main frameworks include Snap (Ubuntu, [Snapcraft](https://snapcraft.io/)), Flatpack ([Flathub](https://flathub.org/)), and [Appimage](https://appimage.org/). These formats simplify software distribution, as each package has all dependencies fully self-contained (and often sandboxed).
- **Terminal.** Command line is really handy! See this [mini-workshop](https://evanwill.github.io/_drafts/notes/commandline.html).
