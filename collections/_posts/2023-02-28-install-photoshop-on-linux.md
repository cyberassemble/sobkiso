---
layout: post
title: "HOW TO INSTALL PHOTOSHOP UNDER LINUX 2023"
date: 2023-02-28T03:22:42Z
authors: ["Sage Kirk", "Mike Vance"]
categories: ["Linux"]
description: "HOW TO INSTALL PHOTOSHOP UNDER LINUX. Make a kali Linux VPS For free, Best way to make a vps server free OS Kali Linux."
thumbnail: "/assets/images/blog/IMG_20230313_033052.jpg"
image: "/assets/images/blog/IMG_20230313_033052.jpg"
comments: false
---

I will show you how to install Photoshop under Linux without any license key. This method is tested under Kali Linux **(debian)**.
**P.S**: The installer works also under Windows.

# HOW TO INSTALL PHOTOSHOP UNDER LINUX

**Github:**

This bash script helps you to install Photoshop CC version 19 on your Linux machine using wine behind the scene and sets some necessary components up for the best performance

### Features

- Downloads necessary components and installs them **(vcrun, atmlib, msxml...)**
- Downloads photoshop.exe installer
- Creates photoshop command and a desktop entry
- Wine dark mode
- Supports graphic cards like (intel, Nvidia)
- Saves the downloaded files in your cache directory
- It's free and you will not need any license key
- Works on any Linux distribution

### Requirements

1. Use a 64bit edition of your distro

2. Make sure the following packages are already installed on your Linux distro

- wine
- wine64
- winetricks
- md5sum

If they are not already installed you can install them using your package manager.

## Arch :
```json
sudo pacman -S wine winetricks
```

## Debian :
```json
sudo apt install wine winetricks
```

3. Make sure you have enough storage in your /home partition about 5 GiB

1 GiB will be free after installation

Also you can install photoshop in diffrent directory

4. Make sure you have an internet connection and about 1.5 Gib traffic to download photoshop and its components

## Installation

The installer scripts use a virtual drive of wine and makes a new winprefix for photoshop.

First of all, you need to clone the repository with this command:

```json
git clone https://github.com/Gictorbit/photoshopCClinux.git
cd photoshopCClinux
```

Then you can easily run setup.sh script to install photoshop cc on your Linux distro

```json
chmod +x setup.sh
./setup.sh
```

> You can use -d to specify the installation path, and -c for the cache directory. For example:

```json
./PhotoshopSetup.sh -d /mnt/myfiles/photoshop
```

**OR**

```json
./PhotoshopSetup.sh -d /mnt/myfiles/photoshop -c /mnt/cache
```

When no options are given, the installer script will use the default path, the uninstaller script and others will detect your custom path so there is no problem, I recommend using the -d option and having the default cache directory. this feature is currently being tested, and will be added to **setup.sh** later

> During installation please pay attention to the script messages

**NOTE** : ==make sure OS version in wine is on windows 7==

Installer script use winetricks to install necessary components

### wineprefix Configuration

If you need to configure the wineprefix of Photoshop you can use winecfg.sh script just run the command below

```json
chmod +x winecfg.sh
./winecfg.sh
```


## Uninstall

To uninstall photoshop you can use the uninstaller script with commands below

```json
chmod +x uninstaller.sh
./uninstaller.sh
```

# How To Install Under Windows

1. Download WinRAR from : [https://www.win-rar.com](https://www.win-rar.com)

1. 1(Optional): Activate WinRAR : [https://t.me/cyberassemble/339](https://t.me/cyberassemble/339)

2. Download installer : [https://victor.poshtiban.io/p/gictor/photoshopCC/photoshopCC-V19.1.6-2018x64.tgz](https://victor.poshtiban.io/p/gictor/photoshopCC/photoshopCC-V19.1.6-2018x64.tgz)

3. Unpack files and run installer, choose path and install it.

4. Enjoy PhotoShop :joy:
