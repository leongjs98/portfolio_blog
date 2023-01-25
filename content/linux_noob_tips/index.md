---
title: "Essential Linux Desktop Terminal Tips for Noobs"
date: 2022-12-14T17:27:46+08:00
draft: true
description: "Essential Tips for Linux Terminal"
summary: "Knowing these tips could save you hours digging through Documents or Google."
tags: ['linux','tech']
---

Whether you like it or not, you have to use the Linux terminal sometimes.
And this guide make sure you save your time.

1. Permission Denied
Anytime you faced with permission issues, run the same command again with sudo in front.
If you don't want to retype the command, use this
```
sudo !!
```

This gives you privillege access to the command, and most of the time, solve your issues.

2. `chmod +x XXX`
AppImage, shell script and many things that you would like to execute.
Make sure they are executable with this command.
