---
title: "Useful Regex Pattern: Fighting One Eyed Kirby"
date: 2023-04-06T16:51:35+08:00
draft: false
description: ""
summary: "Replace and reuse text with regex to save you time while editing codes or texts."
topics: ["Programming", "Productivity"]
---

## Requirements

Any text editors that supports regex. Here I am using Neovim. Other editors
like VSCode should works in similar fashion.

## Command

Things to replace: `\(.*\) \(.*\)`

Replacements: `1: \1 2: \2`

Doesn't `\(.*\)` looks like a one-eyed Kirby ready to throw down? Hence the
name!

`.*` will match everything inside. You can change it to anything else for your
use case.

In Neovim or Vim, this would be the replacement command.
```
%s/\(.*\) \(.*\)/1: \1 2: \2
```

### Before replacing
```
Lorem ipsum
dolor sit
amet, qui
minim labore
adipisicing minim
sint cillum
sint consectetur
```

### After replacing
```
1: Lorem 2: ipsum
1: dolor 2: sit
1: amet, 2: qui
1: minim 2: labore
1: adipisicing 2: minim
1: sint 2: cillum
1: sint 2: consectetur
```
