---
description: >-
  This page will guide you through on how to use WatchThis to jailbreak your
  Kindle that's on firmware 5.12.2.2 or 5.13.4-5.14.2.
---

# WatchThis (5.12.2.2/5.13.4-5.14.2)

Info taken from the original thread: [https://www.mobileread.com/forums/showthread.php?t=346037](https://www.mobileread.com/forums/showthread.php?t=346037)

Before we get started, WatchThis will require you to factory reset your Kindle. Back up your data before proceeding.

In case of the PW3 and KT3: If you're not in the firmware range of WatchThis, you can still jailbreak using [Popcorn](../jailbreak-hardware/popcorn-kt2-kt3-pw2-pw3-kv.md).



## Prerequisites:

This jailbreak is compatible with Kindle devices running the following firmware versions:

| Device                                                                                           | Firmware Versions                                                                                   |
| ------------------------------------------------------------------------------------------------ | --------------------------------------------------------------------------------------------------- |
| <ul><li>PW5</li></ul>                                                                            | <ul><li>5.14.2</li><li>5.14.1</li></ul>                                                             |
| <ul><li>PW4</li><li>KT4</li><li>KT3</li><li>KOA3</li><li>KOA2</li><li>KOA1</li><li>PW3</li></ul> | <ul><li>5.14.2</li><li>5.14.1</li><li>5.13.7</li><li>5.13.6</li><li>5.13.5</li><li>5.13.4</li></ul> |
| <ul><li>KV</li></ul>                                                                             | <ul><li>5.13.6</li><li>5.13.5</li><li>5.13.4</li></ul>                                              |
| <ul><li>KT2</li><li>PW2</li></ul>                                                                | <ul><li>5.12.2.2</li></ul>                                                                          |

You **must** use the exploit payload that matches your device and firmware combination exactly.



## Installation:

### <mark style="color:red;">Please make sure that you've read the entire guide before proceeding.</mark>

#### The Setup:

1. <mark style="color:red;">**Factory reset the device. Make sure to use the "en\_GB" or "English (United Kingdom)" locale when setting the language. Skip Wi-Fi registration by selecting any network then backing out.**</mark>
2. After performing a factory resetType `;enter_demo` in the Kindle search bar.
3. Reboot the device, now it should boot into demo mode. If it doesn't, check [Troubleshooting](watchthis-5.12.2.2-5.13.4-5.14.2.md#troubleshooting).
4. Once in demo mode, skip setting up Wi-Fi and enter dummy values for store registration when prompted.
5. Skip searching for a demo payload.
6. Select the "standard" demo type.
7. Press "Done" at the prompt to sideload content. Do not sideload the jailbreak at this stage.
8.  Once the demo is setup, skip the misconfiguration lockout using the "secret gesture" as shown below:

    <figure><img src="../.gitbook/assets/image.png" alt=""><figcaption><p>2-finger tap on bottom right of screen then swipe left. You may need to try a couple of times.</p></figcaption></figure>
9. Enter the demo configuration menu by typing `;demo` into the search bar.
10. Select the "Sideload Content" option.

#### The Jailbreak:

1. Connect the device to a PC and create the directory `.demo` at the root of the Kindle storage.
2. Copy `${YOUR_DEVICE}-${YOUR_FW_VERSION}.zip` to `.demo/`.
3. Copy `demo.json` to `.demo/`.
4. Create an empty folder at `.demo/goodreads`. Do not put any files in this folder.
5. Press "Done" at the prompt to install the jailbreak script.
   * If an application error occurs, hard reboot the device by holding the power button for 15 seconds or longer, enter the demo menu again and select Sideload Content -> Done once more _without_ connecting to USB.
6. Exit the demo menu and either enter `;dsts` or swipe down and select the settings icon to enter the device settings menu.
   * If jailbreaking KT2 or PW2, select the store button instead.
7. Select "Help & User Guides" then "Get started"
8. The device will reboot, and the jailbreak script will run automatically.

<details>

<summary>Troubleshooting:</summary>

* Alternative Demo Mode entry method:
  * Create an empty file named `DONT_CHECK_BATTERY` at the root of the Kindle USB storage.
  * Activate demo mode by typing `;demo` into the search bar.
  * Once in demo mode, skip setting up Wi-Fi and enter dummy values for store registration when prompted.

<!---->

* If you need to reset your device whilst in Demo Mode, enter `;uzb` in the search bar to enable USB storage mode then create an empty file named `DO_FACTORY_RESTORE` at the root of the Kindle storage. Once this has been created, reboot the device.

<!---->

* If you don't understand how the secret gesture works, here is a [video demonstration](https://www.youtube.com/watch?v=JzuIGbGPpig).

</details>

## Once you've completed everything, and your Kindle is back at the home screen, continue to [Setting up a Hotfix](../post-jailbreak/set-up-a-hotfix.md), following the WatchThis Hotfix tab.
