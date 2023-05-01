---
title: "Chocolatey is how every Windows users should install softwares"
date: 2023-02-16T12:48:42+08:00
draft: false
description: "How to install Chocolatey and why?"
summary: "How and why everyone and their mom should use Chocolatey on Windows."
topics: ["tech", "productivity"]
---

{{< lead >}}
Downloading anything on Windows is a pain. And Chocolatey is here to help.
{{< /lead >}}

I didn't think of this when I was using Windows daily, but downloading anything
on Windows is a pain. And using a package manager like Chocolatey to install
software is way better. 

## Chocolatey

### Installation

The Chocolatey team already has a wonderful
[documentations](https://chocolatey.org/install#individual) for installing it:

But for the people who are petrified by documentations, here is a great
[YouTube video](https://www.youtube.com/watch?v=-5WLKu_J_AE) on installing
Chocolatey by [Hitesh
Choudhary](https://www.youtube.com/@HiteshChoudharydotcom)

### Basic usage

Open your PowerShell in Administrative mode. then run `choco`

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
any help, try the manual.
```
choco help
```

## Why Chocolatey?

### Save your time

Let's say you want to install Firefox, you no longer have to go the the
[official Download](https://www.mozilla.org/en-US/firefox/new/), download the
file, run it and click through everything to get it set up, just use this in
your PowerShell:

```
choco install firefox
```

What happens to the terms and conditions? No one ever reads the terms and
conditions and everyone always keep clicking yes to all the prompts. Chocolatey
knows that and you only have to select yes once using the command above.

#### That's not a lot of time?

Normal users aren't installing new softwares all the time, it's only the devs
are regularly installing new things on their machine. So it's not really saving
a lot of time for the regular users who already have their system set up.

But if you are installing a lot of softwares at once (let's say you are on a
new Windows machine and want all the softwares you had):

You can simply use a line to install the different softwares that you want. For
example:
```
choco install firefox zoom mpv 7zip inkscape brave
```

### Security

And if you are using Google, you run the [risks of getting
malwares](https://www.bleepingcomputer.com/news/security/google-ad-for-gimporg-served-info-stealing-malware-via-lookalike-site/)
if you are not careful enough. Because for whatever reason,  Google does not
vet their ads. There's a high chance of getting malwares disguised as the
softwares that you want.

## How normal Windows users install softwares

Now that you know how to install software the easy way, let's think of how
everyone else install softwares.

1. Search online

2. Find your software

3. Click yes to all the T&C

Most Windows users already grew accustomed to all these steps. And wouldn't
think there's a problem to any of these.

Installing softwares this way is simply inefficient and insecure. The solution
to this is using a package manager. On whichever Linux distro, they have their
own package manager (their own version of Chocolatey), you can simply type in
**one line to search and/or install software.**
