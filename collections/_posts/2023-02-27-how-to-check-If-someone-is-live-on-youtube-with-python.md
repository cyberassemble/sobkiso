---
layout: post
title: "HOW TO CHECK IF SOMEONE IS LIVE ON YOUTUBE Python"
date: 2023-02-27T03:22:42Z
authors: ["Sage Kirk", "Mike Vance"]
categories: ["Development"]
description: "Make a kali Linux VPS For free, Best way to make a vps server free OS Kali Linux."
thumbnail: "/assets/images/blog/Screenshot_2023-02-20-03-28-22-47_40deb401b9ffe8e1df2f1cc5ba480b12.jpg"
image: "/assets/images/blog/Screenshot_2023-02-20-03-28-22-47_40deb401b9ffe8e1df2f1cc5ba480b12.jpg"
comments: false
---

HOW TO CHECK IF SOMEONE IS LIVE ON YOUTUBE [PY]

```python
import requests

def checkChannel(channel_id = None):
    channel_id = "LofiGirl" # put here channel id 
    r = requests.get('https://www.youtube.com/channel/' + channel_id)
    if "hqdefault_live.jpg" in response.text:
        return True
    else:
        return False
checkChannel()
```

Put channel id of the channel, you can find it if you go to the channel and copy the url.. Channel ID is after the /channel/