---
title: "💻 Encrypted Arch - encrypted Arch Linux installer"
date: 2020-07-03T10:51:46+03:00
draft: false
toc: false
categories: ["Security", "GNU Linux", "Bash"]
tags: ["terminal", "application"]
---

**Encrypted Arch** is a semi-interactive script to install Arch Linux over SSH to a fully encrypted disk created using LVM on LUKS. 

## Source code
[Here's the repo :)](https://github.com/elmsec/encrypted-arch). You can star the project to motivate me.


## Highlights
- Full encryption
- Install via SSH
- Format/create disks and partitions with a pre-generated layout file or commands automatically
- GRUB and mkinitcpio configurations:
    - Set hooks and modules dynamically
    - Set GRUB_CMDLINE_LINUX_DEFAULT dynamically
- Create ssh keys and keep them safe
- Desktop: KDE Plasma
- Display Manager: sddm
- UFW firewall rules
- FAI: Except a few questions (passwords, passphrases), fully automatic installer
- ...

## Usage
1. Clone it to your host machine.
2. Set permissions for the files `run.sh`, `./installer/install.sh` and `./installer/chroot.sh` to make them executable: `chmod +x run.sh ./installer/install.sh ./installer/chroot.sh`.
3. Run the `./run.sh` file. It will try to connect to your target machine and run the `./installer/install.sh` script which then runs the `./installer/chroot.sh` when needed.
