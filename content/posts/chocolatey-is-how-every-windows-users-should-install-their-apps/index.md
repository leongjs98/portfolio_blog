---
title: "Chocolatey is how every Windows users should install softwares"
date: 2023-02-16T12:48:42+08:00
draft: false
description: "Why use Chocolatey and how to install and use it on Windows"
summary: "Why and how everyone and their mom should use Chocolatey on Windows."
topics: ["tech", "windows"]
---

{{< lead >}}
Downloading anything on Windows is a pain.
{{< /lead >}}

I didn't think of this when I was using Windows on a daily basis, but
downloading anything on Windows is a pain. And when you grew accustomed to
something, you won't question how bad that thing is and would think that's just
the way that it is.

## How normal Windows users install softwares

1. Search online

2. Find your software

3. Click yes to all the T&C

Most Windows users already grew accustomed to all these steps. And when you
grew accustomed to something, you are not aware of their flaws.

Install softwares this way is simply inefficient and insecure. Using a package
manager is much better. On whichever Linux distro, they have they own package
manager, you can simply type in **one line to search and/or install software.**

Luckily, on Windows, you can use Chocolatey as your package manager.

## Why Chocolatey?

### Save your time

Let's say you want to install Firefox, you don't have to go the the [official
Download](https://www.mozilla.org/en-US/firefox/new/) page anymore, just use
this in your PowerShell:

```
choco install firefox
```

No one ever reads the terms and conditions and everyone always keep clicking
yes to all the prompts. Chocolatey knows that and only have to select yes once.

Or you can simply use `choco install -y firefox`, this is assuming you are
saying yes to everything.

#### That's not a lot of time?

Normal users aren't installing new softwares all the time, it's only the devs
are regularly installing new things on their machine. So it's not really saving
a lot of time for the normies.

But if you are installing a lot of softwares at once (let's say you are on a
new Windows machine and want all the softwares you had):

You can simply use a line to install everything. For example:
```
choco install -y firefox zoom mpv 7zip inkscape brave
```

### Security

And if you are using Google, you run the [risks of getting
malwares](https://www.bleepingcomputer.com/news/security/google-ad-for-gimporg-served-info-stealing-malware-via-lookalike-site/)
if you are not careful enough (for God knows why, Google does not vet the ads
they are promoting). There's a high chance of getting malwares disguised as
the softwares you want.

## Chocolatey

### Installation

The Chocolatey team already has a wonderful
[documentations](https://chocolatey.org/install#individual) for installing it:

But for the people who are petrified by documentations, here are some
instructions with pictures:

Open you Administrative Shell

```
Set-ExecutionPolicy Bypass -Scope Process
```

```
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```

### Basic Usage

For example, to install Firefox, simple run:
```
choco install firefox
```

### Finding softwares

Go to the [Chocolatey Community
Packages](https://community.chocolatey.org/packages) page to search.

Or you can simply search like such:
```
choco find QUERY
```

### Help

Remember RTFM stands for **R**ead **T**hat **F**riendly **M**anual. If you need
any help, try `choco help`
