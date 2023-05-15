---
title: "Download YouTube (or any) videos with yt-dlp"
date: 2023-03-18T23:13:37+08:00
draft: false
description: "Download any video or audio from YouTube or any website with yt-dlp"
summary: "yt-dlp - A Powerful Foss Tool to Download YouTube (and other) Videos"
topics: ["useful foss"]
---

## Installations

### Linux and Mac

For the Linux elitists and Apple users, you can use the command line and
install it with your package manager. I.e. `sudo apt install yt-dlp`

You can also download the [lastest
release](https://github.com/yt-dlp/yt-dlp#release-files) for your OS.

### Windows 

Windows users can also download the [`yt-dlp.exe` release
file](https://chocolatey.org/install#individual).

Or better yet, ditch the old way of downloading anything and use tools like
[`Chocolatey`](https://chocolatey.org/install#individual) (learn more about
[`Chocolatey` from my previoius
post](/posts/chocolatey-is-how-every-windows-users-should-install-their-apps/))
```sh
choco install yt-dlp
```

### Update

If you need the latest version of `yt-dlp` (E.g. stable release distro user),
you can get the lastest version of yt-dlp by downloading the latest [release
file](https://github.com/yt-dlp/yt-dlp#release-files) or run:
```sh
yt-dlp --update
```

## Usage

### Basic: Downloading a video

```sh
yt-dlp "LINK"
# Example
yt-dlp "https://www.youtube.com/watch?v=dQw4w9WgXcQ"
```

{{< alert >}}
Always put quotes to wrap around your link to avoid errors.
{{< /alert >}}

### Common Usage

Command | Function
---|---
`yt-dlp --yes-playlist "LINK"` | Download a playlist of videos
`yt-dlp --extract-audio "LINK"` | Download only the audio
`yt-dlp --extract-audio --yes-playlist "LINK"` | Download a playlist of audios
`yt-dlp --extract-audio --yes-playlist -o "%(playlist_index)s-%(title)s.%(ext)s" "LINK"` | Download a playlist of audios with filename in the pattern of "01-filename.mp3"

### Useful Options

Option | Function
---|---
`--ignore-errors` | Not interrupting the download when encountered errors
`--recode-video mkv` | Change the format of your downloaded video/audio (`mkv` here) (require `ffmpeg`)
`--geo-bypass` | Bypass geographic restrictions
`--playlist-items 4-20` | Only download certain videos from a playlist (4th to 20th here)

### Numbered playlist download

```sh
yt-dlp -o "%(playlist_index)s-%(title)s.%(ext)s" "LINK"
```

This command will download and output your file as ordered in the playlist.
Credit to [Iman
Mohamadi](https://askubuntu.com/questions/694848/how-to-download-a-youtube-playlist-with-numbered-prefix-via-youtube-dl) 

### Need help?

How do I know all these options? Remember the manual is your friend. Hence,
people often says **RTFM**, they just reminding you to **R**ead **T**hat
**F**riendly **M**anual. If you need any help, try the manual first before
searching them online.

```
yt-dlp --help
```

##  Background

`yt-dlp` is a fork of `youtube-dl`, which is a popular YouTube video downloader
in the command line. You can think of `yt-dlp` as the enhanced version of her
predecessor.

Despite the name, they are used to download videos from all kinds of
websites. Use `list-extractors` to know which platform is supported.

### Why yt-dlp over youtube-dl?

`youtube-dl` can be very slow and a lot of times, painfully so.

Most of the time I get less than 100Kb/s when using it. With `yt-dlp`, in the
same environment and WiFi network, I get at least a few Mb/s. The difference is
night and day.
