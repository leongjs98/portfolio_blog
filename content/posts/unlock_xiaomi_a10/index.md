---
title: "No BS Guide to Unlock Xiaomi Redmi 10A Bootloader"
date: 2022-11-04T10:21:53+08:00
draft: false
description: "Learn everything about unlocking Xiaomi Redmi 10A bootloader."
summary: "An actual guide to rooting your Xiaomi A10 bootloader?"
tags: ['tech']
---

## Rooting Xiaomi A10

Rooting this phone is such a pain in the ass. The steps 
weren't straight forward at all. They are really making it 
increasingly a pain to root your phones. It maybe very 
tempting to but please don't root your phone with some 
shady apps.

{{< alert >}}
**Warning!** yada yada security risks, less reliable 
features, void your warranty, risk bricking your phone.
You should know the deal already.
{{< /alert >}}

## Requirements:

-   A Mi Account
    -   need an email and a "recovery phone number"
-   A SIM card with mobile data
-   Intel based Windows PC (I didn't tried it with others)
-   Backup your phone first (if you wanna keep things)
-   Good luck

I don't like the data collection too but hey, what can you 
do?

## Enable developer settings

-   Settings | search About Phone | Keep tapping "MIUI 
version" until a message comes up

In developer options:

1.  enable USB debugging
2.  enable OEM unlocking
3.  Check Unlock Status
    -   bind your Mi account and device as asked

## Mi Unlock

-   Download [Mi Unlock](https://en.miui.com/unlock/download_en.html)
    and unzip it.
-   The program to run is `miflash_unlock.exe`.
-   Never tested but Wine on Linux should run too.

## Boot your phone into fastboot mode

1.  Shutdown your phone
2.  Hold Volume Down + Power Button until "FASTBOOT" comes up

### Run it on your PC

Download the latest version if there is one 

Login your Mi account Give the them your phone number

After agreeing to sacrifice your firstborn child to Satan. 
You will eventually see the unlock screen, just click 
unlock. 

If unlock is disabled, reconnect your device, open
`driver_install.exe` or `driver_install_64.exe`

Wait for 168 hours (7 days) and try again.

-   Don't reset your phone or do other "smart" stuff as mentioned in
    the note section of this [Xiaomi's
    Guide](https://new.c.mi.com/global/post/101245)

## Enjoy

Enjoy your rooted phone. If anything goes bad, go to this
[article](https://new.c.mi.com/global/post/101245), don't try to email
me.

## Sources:

<https://en.miui.com/unlock/download_en.html>
<https://new.c.mi.com/global/post/101245>
