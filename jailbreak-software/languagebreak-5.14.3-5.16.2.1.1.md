---
description: >-
  This page will guide you through on how to use LanguageBreak to jailbreak your
  Kindle on firmware 5.14.3-5.16.2.1.1.
---

# LanguageBreak (5.14.3-5.16.2.1.1)

Info taken from the GitHub repo: [https://github.com/notmarek/LanguageBreak](https://github.com/notmarek/LanguageBreak)

The README in the repo notes that this exploit works best on firmware `5.16.2`, so if you're on an older version, consider [manually upgrading](../miscellaneous/updating-your-kindle-to-a-specific-firmware.md) to 5.16.2(.1.1) first.

<details>

<summary>Warnings/Precautions</summary>

* ⚠️ This method **will** **DELETE** all content on your device. Backup important files.
* ⚠️ This method works up to firmware version `5.16.2.1.1`. It is strongly suggested you upgrade to this firmware before starting.
* ⚠️ Do not update your firmware beyond `5.16.2.1.1` after jailbreaking with LanguageBreak, as future versions of the firmware patch it.
* ⚠️ Your device must have no password lock. Remove it before starting.

</details>

Now before we start, make sure that:

* Airplane Mode is **ON**
* The device (esp. the root folder) should have no `.bin` or `update.bin.tmp.partial` files before you start. This may be a pending OTA update. Delete them.

## Jailbreaking the Kindle

1. Type `;enter_demo` into the Kindle search bar, press enter, then reboot the device.
2. Once the device boots, dismiss the WiFi selection dialog, type whatever you'd like into the text fields, then continue.
3. Select `Skip`, then `Standard`, then `Done`.
4. The device will take a few minutes to go into demo mode. When it's done, use [this gesture](https://www.youtube.com/watch?v=JzuIGbGPpig) to access the main screen. (Tap with 2 fingers on bottom right, then swipe from left to right.)
5. Type `;demo` into the Kindle search bar, then press enter to access the Demo Mode Configuration screen.
6. Select the `Sideload Content` option.
7. Connect your Kindle to a PC, then copy the contents of the `LanguageBreak` folder to the Kindle's root directory (if prompted, overrwrite the existing files).
8. Eject, then _unplug your Kindle_, then return to the Demo Configuration Screen (using the method in step 5, if required).
9. Select `Resell Device`, then confirm.
10. As soon as the "Press the Power Button" screen appears, plug your Kindle back into your computer.
    * You only have a 5-second window, be quick. Generally the best time to plug it in is right before the backlight fades out.
11. Copy the contents of the `LanguageBreak` folder to the Kindle's root directory, again. (if prompted, overrwrite the existing files).
    * From my experience, the Kindle ejects itself after around 30 seconds, so be quick in copying everything.
12. After all files have been written, eject your Kindle, then press and hold the power button until the unit reboots.
13. At this point, a language selection screen appears. Select `简体中文` (Chinese), which should appear above an entry called `Pseudot` and below Japanese.
14. Your Kindle should reboot, and some log messages should appear in the top right-hand corner.

## Applying the Hotfix

_(Normally I would link to_ [_Setting up Hotfix_](../post-jailbreak/set-up-a-hotfix.md)_, but since LanguageBreak also has its own post install procedures, it'll be covered in this page.)_

* Using your phone to translate the menus is helpful if you can't read Chinese.

1. After the device has rebooted, type `;uzb` into the Kindle search bar to enable USB access within demo mode, then press enter.
2. Connect the device to a PC and copy whichever `Update_hotfix_languagebreak-{languge/locale}.bin` file matches your language to the Kindle's root directory.
3. Eject your Kindle, then `;dsts` into the Kindle search bar to access the settings page. Locate the `Update your Kindle` option and press it, then confirm.

This will reboot the device out of Demo mode. Your device may go into Managed mode after completing these steps. Managed devices have some settings greyed out, and ask the user to contact their system administrator. See below for steps on how to restore functionality (and the correct language) to your device.



## Restoring the Correct Language and Exiting Managed Mode

The instruction differs depending if the Kindle has been registered to an Amazon account or not. Click the tab that applies to you.&#x20;

{% tabs %}
{% tab title="If the Kindle is NOT registered to Amazon" %}
1. Type `;demo` into the Kindle search bar.
2. You will get a prompt with two buttons. Press the right-most button.
3. The device will reboot. If all is well, your Kindle should have a folder named `mkk` in the root directory.
{% endtab %}

{% tab title="If the Kindle IS registered to Amazon" %}
1. Enter `;enter_demo` into the Kindle search bar, then reboot your device.
2. The device will be back in full "Demo Mode". Use [the same gesture](https://www.youtube.com/watch?v=JzuIGbGPpig) to access the main screen.
3. Enter `;demo` into the Kindle search bar.
4. Select `Resell device`, then confirm.
5. The device will reboot. If all is well, your Kindle should have a folder named `mkk` in the root directory.
{% endtab %}
{% endtabs %}

<details>

<summary>Frequently Asked Questions (FAQ)</summary>

Q: How do I verify my installation? \
A: (before applying hotfix): Install hotfix, if you can do that then it worked. \
A: (after applying hotfix): Type `;log` into the Kindle search bar, some text should appear at the top right side of the screen.

Q: Where are the hotfix files? \
A: The structure of the tarball is as follows:

```
LanguageBreak.tar.gz
|-- LanguageBreak
|	|-- documents
|	|	|-- dictionaries
|	|	|	|-- a; export SLASH=$(awk 'BEGIN {print substr(ARGV[1], 0, 1)}' ${PWD}); sh ${SLASH}mnt${SLASH}us${SLASH}jb
|	|	|	|-- amisane
|	|-- DONT_CHECK_BATTERY
|	|-- jb
|	|-- patchedUks
|	|-- .demo
|	|	|-- boot.flag
|-- Update_hotfix_languagebreak-*.bin
```

</details>

<details>

<summary>Troubleshooting</summary>

Having general issues?

This method works best around firmware version `5.16.2`. Consider updating to this version to avoid compatability issues by following [this guide](../miscellaneous/updating-your-kindle-to-a-specific-firmware.md).

**To install the file, place it into the root directory of the Kindle, then select `Update your Kindle` in settings. It should also apply the update on reboot if the menu is inaccessible for some reason.**

</details>

### [Consider buying Marek a coffee if this helped you!](https://ko-fi.com/notmarek)

## Once you're done, continue with [Installing KUAL/MRPI](../post-jailbreak/installing-kual-mrpi.md).
