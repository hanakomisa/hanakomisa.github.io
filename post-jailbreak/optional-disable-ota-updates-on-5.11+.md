---
description: This page will guide you through how to disable OTA updates on the Kindle.
---

# (Optional) Disable OTA Updates on 5.11+

Since `5.11.x`, it has become increasingly harder to block software updates. The old method of putting a folder named `update.bin.tmp.partial` no longer works, so we'll need to improvise in other ways.

## Using hius07's renameotabin KUAL extension:

1. Download the [renameotabin](https://www.mobileread.com/forums/showpost.php?p=4076733\&postcount=25) extension.
2. Plug in your Kindle to your computer (Make sure that USBNetwork is disabled!), drag the `renameotabin` folder into `extensions` on your Kindle's drive.
3. Eject then unplug your Kindle from your computer.
4. Go into KUAL, Tap on `Rename OTA Binaries`
5. Tap on `Rename`, your Kindle will reboot.
6. That should be it. Now if you put in an update file in the root of your Kindle's storage, the update button should still be greyed out. Do note that if you're planning to factory reset, don't forget to repeat step 4 and 5, but do `Restore` instead of `Rename`.

<details>

<summary>Blocking OTA updates on 5.10.x and older versions:</summary>

Simply create a folder called `update.bin.tmp.partial` in your Kindle's visible storage's root, and make sure to set it to read-only.

</details>

## Once you've finished, congratulations! Your Kindle now has full jailbreak and updates blocked. If you're looking for KOReader, simply press the Next button down below.
