Title: File Syncing and Backups on Windows With Robocopy
Date: 21 Oct, 2019
Keywords: self hosted,windows,robocopy,rsync,backups,file sync

Robocopy is a native Windows tool for syncing files and folders. This guide is aimed at (ex-) Linux/Mac users who want a native Windows solution to syncing/mirroring folders like Rsync.

Keep in mind that Robocopy is not a feature-by-feature replacement for Rsync and **does NOT natively support syncing over SSH**. It does, however allow syncing with Network Shares (SMB/CIFS).

Table of Contents:
<!-- TOC -->

- [Basic folder syncing](#basic-folder-syncing)
- [Mirroring](#mirroring)
    - [Other useful options](#other-useful-options)
- [Resources](#resources)

<!-- /TOC -->
## Basic folder syncing

To start, open a PowerShell window.

Robocopy commands are structured like:

    robocopy <source> <destination> [<options>]

To sync a folder in your Home directory to an external drive (H:) :

    robocopy ~\Documents H:\backups\Documents /s

This syncs the folder "Documents" in `~`, which is your user's home directory (`C:\Users\yourUsername` by default) with `H:\backups\Documents`. The `/s` option tells Robocopy to copy **s**ubdirectories when available. This however does not sync empty directories.

If you also want empty subdirectories to be synced, use `/e` :

    robocopy ~\Documents H:\backups\Documents /e

To copy all file information (time stamps, owner information etc), use the `/copy:datso` option ( **D**ata, **A**ttributes, **T**imestamps, **S**ecurity, **O**wner info):

    robocopy ~\Documents H:\backups\Documents /copy:datso /e
 

## Mirroring

To mirror a folder, use the `/mir` option. This will delete destination files and directories that do not exist in the source :

    robocopy ~\Documents H:\backups\Documents /mir
 

### Other useful options

* `/lev:<n>` : Copies only the top `n` levels of the source directory tree.
* `/xf <filename>` : Excludes files that match the specified names or paths. Supports wildcard characters (* and ?).
* `/xd <directory>` : Same thing, but for directories.
* `/xo` : Excludes older files. Use if you do not want Robocopy to replace the files in destination if they are newer than the source.
* `/max:<n>` : Specifies the maximum file size. Excludes files bigger than `n` bytes.
* `/min:<n>` : Specifies the minimum file size.
* `/maxage:<n>` : Specifies the maximum file age. Excludes files older than `n` days or date.
* `/minage:<n>` : Specifies the minimum file age.
 

## Resources
* [Microsoft Docs Page for Robocopy](https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/robocopy)
* [Wikipedia Article](http://en.wikipedia.org/wiki/Robocopy)