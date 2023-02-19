---
layout: post
title: "How to Setup Termux In Android full 2023"
date: 2023-02-13T09:49:03Z
authors: ["Mike Vance"]
categories: ["Pentesting"]
description: Tutorial About, How to setup termux in Android smartphone for PenTesting and use all tools.
thumbnail: "/assets/images/blog/IMG_20230220_044004.jpg"
image: "/assets/images/blog/IMG_20230220_044004.jpg"
comments: false
subscribe: true
---

In this tutorial we will show you how you can setup termux in Android for PenTesting. and use all Python tool and other tool.

First of all Download Termux apk from our telegram channel. *Not from play store*.

Download link: [Here](https://t.me/cyberassemble/578)

Then open Termux app

Like this

![Termux](/assets/images/blog/Screenshot_2023-02-20-04-44-32-60_84d3000e3f4017145260f7618db1d683.jpg)

Then peste all this Commands

Commands :-(copy paste this in your termux) 
```python
apt update && apt upgrade && pkg install python && pip install colorama && pip install requests && pip install telethon && pip install licensing && pip install rich && python3 -m pip install --upgrade pip setuptools wheel
```

like this.
![Termux cmd](/assets/images/blog/Screenshot_2023-02-20-04-44-52-64_84d3000e3f4017145260f7618db1d683.jpg)

then hit enter. *and perss y*
![Termux cmd 1](/assets/images/blog/Screenshot_2023-02-20-04-45-14-06_84d3000e3f4017145260f7618db1d683.jpg)

Now all file are installing

![Termux cmd 2](/assets/images/blog/Screenshot_2023-02-20-04-46-31-86_84d3000e3f4017145260f7618db1d683.jpg)

Now lets try a tool.

we are going to git clone this tool. like this.

```git clone https://github.com/jsbueno/terminal_matrix```

now ```cd terminal_matrix```

![Tool](/assets/images/blog/Screenshot_2023-02-20-05-01-34-24_84d3000e3f4017145260f7618db1d683.jpg)

now for run this tool type ```python matrix.py```

![Tool](/assets/images/blog/Screenshot_2023-02-20-05-01-59-73_84d3000e3f4017145260f7618db1d683.jpg)

and voooola.

Your termux apk us working fine.


Thank you for today, See you in next tutorial. you can join our telegram channel. for more content.
