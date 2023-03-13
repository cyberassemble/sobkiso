---
layout: post
title: "How install kali Linux Installing Kali Linux on Windows 10/11"
date: 2023-03-11T03:22:42Z
authors: ["Sage Kirk"]
categories: ["Linux"]
description: "In this tutorial we will khow how install kali Linux Installing Kali Linux on Windows 10/11. This is the easy way and best method for you. Follow this tutorial cearfully."
thumbnail: "/assets/images/blog/IMG_20230313_044717.jpg"
image: "/assets/images/blog/IMG_20230313_044717.jpg"
comments: false
---

In this tutorial we will khow how install kali Linux Installing Kali Linux on Windows 10/11. This is the easy way and best method for you. Follow this tutorial cearfully.

so Let's get started. Let's begin.

# **Kali Linux** Installing Kali Linux on Windows 10/11 **TUT**

Installing Kali Linux without external drives, third-party programs. Only Windows resources will be used, more specifically **"Windows SubSystem Linux"**.

## Activate WSL:

1. Launch PowerShell as Admin

2. I write the command:

> Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux

3. Download the updated kernel package

[](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi)

4. Enter the command in PowerShell:

```wsl --set-default-version 2```

5. Go to the Microsoft Store and download Kali Linux 

[](https://imgur.com/a/QajDn5b)

6. Update:

Enter commands:

```js
export LANG=C
```

```js
sudo apt-get update
sudo apt-get dist-upgrade
sudo apt-get clean
```

7. GUI Shell

We enter the command:

```sudo apt update && sudo apt install -y kali-win-kex```


(After installation, to run the graphical shell, just enter the command in Kali - kex In order to remove it, use the command - kex kill ) 

8. Installing git

We write commands in kali:

```sudo apt install git```

### You can also install it on Windows if [](https://git-scm.com/download/win doesn't work)

9. Installing python 

````js
sudo apt update
sudo apt -y upgrade
sudo apt install python3
sudo apt install python2
sudo apt install -y python3-pip
pip3 install numpy
sudo apt install build-essential libssl-dev libffi-dev python3-dev
```
```
python3 -V
python2 -V
```
**(version check)**