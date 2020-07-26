# Welcome to The Self-host Wiki

## What

This is a wiki dedicated to help people run services such as file
servers, NAS, backup servers, seedboxes etc on their own hardware and
local network.

## Why

While the above services are available easily and for free (or for a
small monthly subscription) by companies such as Google, Apple, Dropbox
etc., there are issues such as privacy, non-availability due to loss of
internet connection, and government censorship. Companies can terminate
accounts for undisclosed reasons, accounts can
get hacked, trade wars can prohibit companies from providing their services to other countries, and internet lines can go out due to accidents or natural disasters.

Even for people who are not concerned about the above issues, self hosting can be
a fun exercise in DIY, an extra backup plan in addition to cloud
services, or salvaging older, unused hardware such as obsolete
smartphones, abandoned Raspberry Pis, and laptops with low-res or broken
screens/batteries. Such devices can often make perfectly usable,
low-powered servers instead of rotting away in a basement, or worse, in a
landfill.

## For whom

The intended audience is people who are not afraid to dive into the
command line, but also do not have the time or mental space to look up
tutorials that might be obsolete, scattered across the web, or for a
different distribution than they run. The guides are aimed to be as
much "copy and paste commands as-is" as possible while not compromising
on security.

## How

This wiki will primarily focus on two platforms: the latest version of
Debian GNU/Linux (the instructions for which will usually run unmodified
on Ubuntu LTS, and will be noted where they don't), and [Windows
Subsystem for Linux](http://en.wikipedia.org/wiki/Windows_Subsystem_for_Linux) (WSL). The reason for the latter (certainly
controversial) choice is to enable people who have a working Windows 10
system to be able to run software like [NextCloud](https://nextcloud.com/) or [Syncthing](https://syncthing.net/) without
having to commit a different machine, hard disk or switching over
completely to Linux.

## Topics to be covered

Here is a tentative list of topics that will be covered at first. The
list wil grow bigger in scope as time goes on:

-   [Simple File Server Using SMB and NGINX](guides/fileserver.md) \[RPi/Debian/WSL\]
-   [Automated, Distributed Local Backups Using Syncthing and Rsync](guides/sync_backup.md)
    \[RPi/Debian/Windows/Android\]
-   [Simple Torrent Box Using Transmission-daemon](guides/torrentbox.md) \[RPi/Debian/Ubuntu\]
-   Mobile Torrent Box Using LibreTorrent \[Android\]
-   ...more to come
