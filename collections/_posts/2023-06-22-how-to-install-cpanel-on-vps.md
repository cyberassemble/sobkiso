---
layout: post
title: "How to install Cpanel/WHM on VPS"
date: 2023-06-22T03:22:42Z
authors: ["Sage Kirk", "Mike Vance"]
categories: ["Hosting", "Development"]
description: "Make a kali Linux VPS For free, Best way to make a vps server free OS Kali Linux."
thumbnail: "/assets/images/blog/Screenshot_2023-02-20-03-28-22-47_40deb401b9ffe8e1df2f1cc5ba480b12.jpg"
image: "/assets/images/blog/Screenshot_2023-02-20-03-28-22-47_40deb401b9ffe8e1df2f1cc5ba480b12.jpg"
comments: false
---

# How to install Cpanel/WHM on VPS ✅

## What is Cpanel/WHM?

cPanel & WHM allows hosting providers and users the ability to automate server management tasks while offering your customers the tools they need to manage their sites.

**Prerequisite:**
▪️cPanel & WHM should be installed on a freshly-installed operating system.
▪️Access the VPS via SSH with root user.
▪️Run following commands on shell or terminal (All commands run need to be as root user only)
▪️You need to purchase your own cPanel license to use the control panel.

Instruction to install Cpanel/WHM:

1️⃣ Set a Valid hostname for your VPS using below command.

hostname <hostname for your VPS eg. Example.com>

hostname testvpn.com.net

2️⃣ Disable SELinux on your VPS using below command :

sed -i 's/SELINUX=enforcing/SELINUX=disabled/' /etc/selinux/config 

3️⃣ Download and run below script to install the Cpanel/WHM and let the installation to be completed.

cd /home && curl -o latest -L https://securedownloads.cpanel.net/latest && sh latest

4️⃣ Set a complex password for your WHM

passwd root

As the installation gets completed you can access to your WHM account referring the below details: 

URL: https://<Your server IP>:2087
Username: root
Password: Password of your root user

(Note: You can run installation in screen in order to avoid disconnection to the server)

For port management of Cpanel you can refer to their official URL: https://documentation.cpanel.net/display/CKB/How+to+Configure+Your+Firewall+for+cPanel+Services