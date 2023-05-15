---
title: "Quickly tag music and audio files in terminal with id3"
date: 2023-04-27T13:48:59+08:00
draft: false
description: "Terminal tool to quickly tagging music with ID3 metadata. Automated."
summary: "Terminal tool to tag music with ID3 metadata"
topics: ["Useful FOSS", "Digital Productivity"]
---

`id3` is available in Linux, Windows and MacOS. Make sure you install
**latest** id3 (v0.80 as of writing) from
https://squell.github.io/id3/#getting-it

## Basic `id3` usage

Let's say you have the album ["Melophobia" by Cage The
Elephant](https://www.youtube.com/playlist?list=OLAK5uy_kdMzcHs_e8Bfxkcuy-TxFmwqoUGxtqAYg)
as below:
```
├── 01-Spiderhead.ogg
├── 02-Come A Little Closer.ogg
├── 03-Telescope.ogg
├── 04-It's Just Forever.ogg
├── 05-Take It Or Leave It.ogg
├── 06-Halo.ogg
├── 07-Black Widow.ogg
├── 08-Hypocrite.ogg
├── 09-Teeth.ogg
└── 10-Cigarette Daydreams.ogg
```

### Tagging album

Go into your terminal, then run:
```
id3 --album "Melophobia" *
```

### Tagging year

Go into your terminal, then run:
```
id3 --year "2013" *
```

### Tagging artist

Go into your terminal, then run:
```
id3 --artist "Cage the Elephant" *
```

### Tagging genre

To tag the genre, please refer to the table at the end of this page.
The number 41 is for "Alternative Rock".

Go into your terminal, then run:
```
id3 --genre "41"
```

### Tagging track number 

You can tag the track number of each file one by one with:
```
id3 --track 1 FILENAME
```

### Tagging title

You can tag the title of each file one by one with:
```
id3 --title "TITLE" FILENAME
```

### Powerful `--match` option

the option `--match` is the most powerful option of this program. Please read the
manpage if you are interested in the details

Or if you have your the track number in your filenames with the pattern
`01-Spiderhead.ogg`. Go into your terminal, then run:
```
id3 --match "%T-%t.ogg"
```

Note that `--match` require using the shorthands of the ID3 tag name `T` is
short for "track" and `t` is short for "title". 

### All of the above
You can tag all ID3v1 information in one line:

```
id3 --album "Melophobia" --year "2013" --genre "41" --artist "Cage the Elephant" --match "%T-%t.ogg"
```

### Help yourself

```
id3 --help
```

## ID3v1 genre list

| Number | Genre |
| --- | --- |
| 01 | Blues |
| 02 | Classic rock |
| 03 | Country |
| 04 | Dance |
| 05 | Disco |
| 06 | Funk |
| 07 | Grunge |
| 08 | Hip-Hop |
| 09 | Jazz |
| 10 | Metal |
| 11 | New Age |
| 12 | Oldies |
| 13 | Other |
| 14 | Pop |
| 15 | Rhythm and Blues |
| 16 | Rap |
| 17 | Reggae |
| 18 | Rock |
| 19 | Techno |
| 20 | Industrial |
| 21 | Alternative |
| 22 | Ska |
| 23 | Death metal |
| 24 | Pranks |
| 25 | Soundtrack |
| 26 | Euro-Techno |
| 27 | Ambient |
| 28 | Trip-Hop |
| 29 | Vocal |
| 30 | Jazz & Funk |
| 31 | Fusion |
| 32 | Trance |
| 33 | Classical |
| 34 | Instrumental |
| 35 | Acid |
| 36 | House |
| 37 | Game |
| 38 | Sound clip |
| 39 | Gospel |
| 40 | Noise |
| 41 | Alternative Rock |
| 42 | Bass |
| 43 | Soul |
| 44 | Punk |
| 45 | Space |
| 46 | Meditative |
| 47 | Instrumental Pop |
| 48 | Instrumental rock |
| 49 | Ethnic |
| 50 | Gothic |
| 51 | Darkwave |
| 52 | Techno-Industrial |
| 53 | Electronic |
| 54 | Pop-Folk |
| 55 | Eurodance |
| 56 | Dream |
| 57 | Southern Rock |
| 58 | Comedy |
| 59 | Cult |
| 60 | Gangsta |
| 61 | Top 40 |
| 62 | Christian Rap |
| 63 | Pop/Funk |
| 64 | Jungle |
| 65 | Native US |
| 66 | Cabaret |
| 67 | New Wave |
| 68 | Psychedelic |
| 69 | Rave |
| 70 | Show tunes |
| 71 | Trailer |
| 72 | Lo-Fi |
| 73 | Tribal |
| 74 | Acid Punk |
| 75 | Acid Jazz |
| 76 | Polka |
| 77 | Retro |
| 78 | Musical |
| 79 | Rock 'n' Roll |
| 80 | Hard rock |
| 81 | Folk |
| 82 | Folk-Rock |
| 83 | National Folk |
| 84 | Swing |
| 85 | Fast Fusion |
| 86 | Bebop |
| 87 | Latin |
| 88 | Revival |
| 89 | Celtic |
| 90 | Bluegrass |
| 91 | Avantgarde |
| 92 | Gothic Rock |
| 93 | Progressive Rock |
| 94 | Psychedelic Rock |
| 95 | Symphonic Rock |
| 96 | Slow rock |
| 97 | Big Band |
| 98 | Chorus |
| 99 | Easy Listening |
| 100 | Acoustic |
| 101 | Humour |
| 102 | Speech |
| 103 | Chanson |
| 104 | Opera |
| 105 | Chamber music |
| 106 | Sonata |
| 107 | Symphony |
| 108 | Booty bass |
| 109 | Primus |
| 110 | Porn groove |
| 111 | Satire |
| 112 | Slow jam |
| 113 | Club |
| 114 | Tango |
| 115 | Samba |
| 116 | Folklore |
| 117 | Ballad |
| 118 | Power ballad |
| 119 | Rhythmic Soul |
| 120 | Freestyle |
| 121 | Duet |
| 122 | Punk Rock |
| 123 | Drum solo |
| 124 | A cappella |
| 125 | Euro-House |
| 126 | Dancehall |
| 127 | Goa |
| 128 | Drum & Bass |
| 129 | Club-House |
| 130 | Hardcore Techno |
| 131 | Terror |
| 132 | Indie |
| 133 | BritPop |
| 134 | Negerpunk |
| 135 | Polsk Punk |
| 136 | Beat |
| 137 | Christian Gangsta Rap |
| 138 | Heavy Metal |
| 139 | Black Metal |
| 140 | Crossover |
| 141 | Contemporary Christian |
| 142 | Christian rock |
| 143 | Merengue |
| 144 | Salsa |
| 145 | Thrash Metal |
