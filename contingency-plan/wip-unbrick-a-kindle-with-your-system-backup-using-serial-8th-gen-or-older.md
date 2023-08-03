---
description: >-
  This page will guide you through how to unbrick a Kindle with the system files
  you have backed up in a prior stage.
---

# WIP: Unbrick a Kindle with your system backup using Serial (8th gen or older)

This guide will only cover how to restore your RootFS to make the system work again, it may expend to cover fringe cases of broken DIAGS partition and other things in the future. Functionally, this is very identical to the guide [forcing the Voyage to run 5.14+ firmware versions](../miscellaneous/forcing-kv-to-run-5.14+.md).

You will need a serial connection. The guide doesn't cover this yet but I would expect that you can do some googling to find how to, this is an advanced method so you'll need to know a bit of computer-wizardry.

* TL;DR, get a 1.8v Serial to USB adapter. Solder it to the pads on your Kindle's motherboard.&#x20;
* The usual settings are 115200bps.

## Prerequisites:

* A bricked Kindle with a broken RootFS.
* Your backup. Alternatively [extract a RootFS](../miscellaneous/forcing-kv-to-run-5.14+.md#process) from an update file using [KindleTool](https://github.com/NiLuJe/KindleTool).

## How to unbrick:

1. Power your Kindle on, then interrupt the boot process through the serial terminal.
2. When you get the `uboot >` prompt, boot into `DIAGS` by typing `bootm 0xE41000`.
3. Once you're in `DIAGS`, export the userspace partition: `usb export`
4. Transfer your backed up, or extracted RootFS to your device.
5. Once it's done, eject the Kindle from your PC, then exit USB Export mode.
6. Exit diags mode, and drop into a shell: `exit login`
7. Flash your RootFS using DD, this will take a while: \
   `dd if=/mnt/us/`**`<rootfs file name>.img`**` ``of=/dev/mmcblk0p1 bs=4096`\
   Obviously, change `<rootfs file name>` to whatever you have it named.
8. Once it finishes, reboot your device: `reboot`

## Hopefully if everything goes right, your Kindle should boot back into your system.

