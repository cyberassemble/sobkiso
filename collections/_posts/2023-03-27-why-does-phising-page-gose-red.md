---
layout: post
title: "#"
date: 2023-03-27T03:22:42Z
authors: ["Mike Vance"]
categories: ["Development"]
description: "#"
thumbnail: "/assets/images/blog/Screenshot_2023-02-20-03-28-22-47_40deb401b9ffe8e1df2f1cc5ba480b12.jpg"
image: "/assets/images/blog/Screenshot_2023-02-20-03-28-22-47_40deb401b9ffe8e1df2f1cc5ba480b12.jpg"
comments: false
---

🔴 WHY DOES PHISHING PAGES GOES RED 🔴

In this post we will discover few points of this topics. 

First of all, phishing pages are coded to harm people. That's are fact number 1. Second your page is not red, because of the login form, no, every site on the www (world wide web) has a login form. A login form is normal in our internet modern times if not already a standard of every website.

What is the term RED ?

This term is just saying that your page is detected as harmful and deceptive.

An example of such a message is : 
https://i.imgur.com/738txE2.png

According to Google, there are several types :

The site ahead contains malware: The site you start to visit might try to install bad software, called malware, on your computer.
Deceptive site ahead: The site you try to visit might be a phishing site.
Suspicious site: The site you want to visit seems suspicious and may not be safe.
The site ahead contains harmful programs: The site you start to visit might try to trick you into installing programs that cause problems when you’re browsing online.
This page is trying to load scripts from unauthenticated sources: The site you try to visit isn't secure.

Important: Download with caution. Some sites try to trick you into downloading harmful software by telling you that you have a virus. Be careful not to download any harmful software.

Source : https://support.google.com/chrome/answer/99020?hl=en&co=GENIE.Platform%3DDesktop

The question comes now, how the hell then Google Safebrowsing recognizes my site as phishing ??!

Well, that is simple to answer :
The code matters, but not always.

Why not always?

I've also had phishing pages that had 'bot' and 'victim' traffic, and didn't turn red, and the code was 1:1 from the original website.

Now let's deal with a few other points.

How is our site selected according to the safebrowsing principle and does my site have anything to do with it, e.g. Antibots?

Usually, Antibots were coded, to block a bunch of IP ranges, Crawlers and Bots. Bot traffic is like a virus, nobody wants it. Bot traffic fills on bad coded pages empty forms out, continue without clicking submit button and fills your mail with empty logs. Another reason to use Antibots is also to avoid web security scanner and analyzer to explore our page.

So what happens when a bot passes our antibots?

This is not bad at all if the page has a good anti skip form validation like our Scarletta pages. But if this happens you will get empty logs as i already said, copy the IP and report this IP to @f4c3r100. The seller might also sold you an old page or the bot is a really good humanized bot!

Does my site have any damage like RED after passing a bot?

As a usual case, no. It can happen if a lot of bots happen that it comes to this, but by a single one you can not make yourself a picture of the whole site as an anti-phishing company because there are now times false posivites.

What does Safebrowsing pay attention to ?

▪️URL
▪️HTML Code
▪️Resource file names (CSS, JS, IMAGES...)
▪️Post Field Values (username, password ....)
▪️Known HTML Comments Of Coders 
▪️Drops If Invalid Actions Are Done (like 404 page, die or exit in PHP*)
▪️Does The Application/Page Looks Suspicious ?
▪️Phishing Terms Found ?

* Dropping 404 errors are also suspicious to google, they notice that they have an error and try to visit the page maybe multiples times. 

It is important to note that Safebrowsing is built into every browser.

To disable safebrowsing in Firefox follow this :
https://t.me/c/1154385673/446

We don't learn much about Antibots from this post, yet why the site can be recognized as Suspect and Red.

✨ Credits : https://t.me/tutorials_zone