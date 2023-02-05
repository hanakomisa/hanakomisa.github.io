---
description: >-
  This page will guide you through on how to back up your Kindle's system
  partitions, in case of a brick so that you can restore it to a functional
  state using a serial connection.
---

# Back up your Kindle's system files (8th gen or older)

This guide will only apply to older devices such as the PW2, PW3, KT2, KT3, KV, KOA as newer devices such as the PW4/KT4 has a different partition layout, alongside secure boot, thus no way to restore it even if you have managed to back up the entire system.

## Prerequisites:

* Jailbroken Kindle with KUAL installed.
* [kterm](https://github.com/bfabiszewski/kterm), a terminal emulator for your Kindle.
* knc1's [Kindle Backup script](https://www.mobileread.com/forums/showthread.php?t=289690).

## How to use:

1. First, install `kterm` to `extensions` on your Kindle. This will allow `kterm` to be launched from KUAL. (Drag and drop the kterm folder to extensions!)
2. Unarchive `backup-0.3.tar.gz`, Plug in your Kindle (with USBNetwork turned off, if you don't know what this is feel free to ignore.) and then copy both `esys` and `unjail` folders to the root of your Kindle's visible storage (it's where the `documents` folder is).
3. Eject your Kindle, then go to `KUAL` > `kterm`.
4.  Do the following:

    1. `cd /mnt/us/unjail`
    2. `ls` to make sure that the script is there.
    3. Once you've verified the script is there, `./mkbackup.sh`.
    4. This will take a few minutes. Sit back, relax, and have a cup of tea, or beer if that's more your thing.
    5. Once it's done, it'll create a folder called `backups` in the visible storage of Kindle (`/mnt/us/backups`) in which you can find your backup.
    6. Exit `kterm` by doing `exit`, then plug your Kindle back in.
    7. Copy the contents inside of `backups` to a safe place.



## That's it, you've backed up the important system files! In case your Kindle ever bricks itself (which sometimes can happen), follow [this guide](wip-unbrick-a-kindle-with-your-system-backup-using-serial-8th-gen-or-older.md).&#x20;
