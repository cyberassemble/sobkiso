---
layout: post
title: "How To make free RDP 2023 - Method Free RDP (Lifetime)"
date: 2023-03-08T03:22:42Z
authors: ["Mike Vance"]
categories: ["Hosting"]
description: "In this tutorial i will show you, How to get a Free RDP (Remote Desktop Connection) For Free Lifetime. This is the easy way to make a RDP For Free And 100% Working."
thumbnail: "/assets/images/blog/IMG_20230313_061147.jpg"
image: "/assets/images/blog/IMG_20230313_061147.jpg"
comments: false
---

In this tutorial i will show you, **How to get a Free RDP (Remote Desktop Connection)** For Free Lifetime. This is the easy way to make a RDP For Free And 100% Working.

# Method Free RDP

1. Account must be created at: [](https://dashboard.ngrok.com/signup)

2. Go to **"Settings"** then **"Secrets"** and create a secret repository named ```NGROK_AUTH_TOKEN```

Place the token: [](https://dashboard.ngrok.com/get-started/your-authtoken in the secret repository)

3. Now go to Github and Create a repo then Create a file in you github repo.

Name **.github/workflows/rdp.yml**

peste this code.

```yml
name: CI

on: [push, workflow_dispatch]

jobs:
  build:

    runs-on: windows-latest

    steps:
    - name: Download
      run: Invoke-WebRequest https://bin.equinox.io/c/4VmDzA7iaHb/ngrok-stable-windows-amd64.zip -OutFile ngrok.zip
    - name: Extract
      run: Expand-Archive ngrok.zip
    - name: Auth
      run: .\ngrok\ngrok.exe authtoken $Env:NGROK_AUTH_TOKEN
      env:
        NGROK_AUTH_TOKEN: ${{ secrets.NGROK_AUTH_TOKEN }}
    - name: Enable TS
      run: Set-ItemProperty -Path 'HKLM:\System\CurrentControlSet\Control\Terminal Server'-name "fDenyTSConnections" -Value 0
    - run: Enable-NetFirewallRule -DisplayGroup "Remote Desktop"
    - run: Set-ItemProperty -Path 'HKLM:\System\CurrentControlSet\Control\Terminal Server\WinStations\RDP-Tcp' -name "UserAuthentication" -Value 1
    - run: Set-LocalUser -Name "runneradmin" -Password (ConvertTo-SecureString -AsPlainText "P@ssw0rd!" -Force)
    - name: Create Tunnel
      run: .\ngrok\ngrok.exe tcp 3389
```

3. Go to **"Actions"** and look for **"RDP"** for Windows or **"server"** for Linux.

IP: [dashboard.ngrok.com](https://dashboard.ngrok.com/endpoints/status)
Time: 6 hours
Config windows.
client: RDP
User: rapmind
Password: tester2022
Config linux

**Read Also [HOW TO GET TRAFFIC FROM TIK TOK USING LOGS AND AUTO REGS](/blog/2023-03-12-how-to-get-trafic-from-tiktok/)

~~YOU CAN GET DISABLED ACTIONS!!!!~~

> client: any ssh client
User: user
Password: toor
Config. PC
RAM: 7gb
Cores: 2
