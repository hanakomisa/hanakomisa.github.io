---
description: >-
  This page will guide you through how to downgrade your Kindle firmware with
  this KUAL extension.
---

# Downgrading your Kindle Firmware

Info taken from original thread: [https://www.mobileread.com/forums/showthread.php?t=347165](https://www.mobileread.com/forums/showthread.php?t=347165)

## Prerequisites:

* A Jailbroken Kindle with KUAL installed.
* [Firmware version of your device that you desire](updating-your-kindle-to-a-specific-firmware.md).
* [Downgrader](https://www.mobileread.com/forums/attachment.php?attachmentid=194079\&d=1654169165) KUAL extension.
* Backed up data as well as your [system files](../contingency-plan/back-up-your-kindles-system-files-8th-gen-or-older.md), as downgrading your Kindle can corrupt things.

## How To Downgrade:

1. Before you proceed, if you have [disabled OTA updates](../post-jailbreak/optional-disable-ota-updates-on-5.11+.md), restore it now to prevent complications later.
2. Install the Downgrader extension as you would any other KUAL extension.&#x20;
   * Drag and drop the `downgrader` folder containing the `bin`, `config.xml`, `menu.json` into the `extensions` folder on your Kindle's visible storage's root.
3. Launch KUAL, then Downgrader.
4. Pick the device that you have, make sure it is the right device as this tool sets up the `version.txt` file to match that of the lowest denominator of the device, thus tricking the Kindle's updater to force an "upgrade".
5. Once you've selected your device, your Kindle will restart, now with the lowest version possible spoofed in the system.&#x20;
6. Plug in your Kindle (making sure that USBNetwork is off and USBMS is on), then copy the update file you've downloaded earlier to the Kindle's visible storage root.
7. <mark style="color:red;">**DO NOT**</mark> <mark style="color:red;">eject or unplug the USB cable</mark>, as this will make the Kindle's OS auto delete the update file we just copied to. Instead, hold the power button until your Kindle restarts. Now it should boot into the updater, and begins your firmware downgrade.

## That's it, you've downgraded your Kindle! Note that you should factory reset, then flash that firmware once again to clear out things.
