---
description: >-
  This page will guide you through setting up KUAL (Kindle Unified Application
  Launcher) and MRPI (MobileRead Package Installer) to install and use homebrew
  on your Kindle.
---

# Installing KUAL/MRPI

Info taken from the original thread: [https://www.mobileread.com/forums/showthread.php?t=320564](https://www.mobileread.com/forums/showthread.php?t=320564)

Note that KUAL (Booklet) and MRPI depends on each other, so you will have to install both of them at the same time.

## Prerequisites:

* KUAL and MRPI, download them from [NiLuJe's snapshot thread](https://www.mobileread.com/forums/showthread.php?t=225030).
  * There are multiple variants of KUAL as it is designed to run across the _entire_ range of Kindles. For which variants to pick for your Kindle:
    * For FW 5.9 and newer, use **KUAL Booklet (coplate)** variant.
    * For FW 5.8.x and older, use **KUAL Booklet** variant**.**

## Installation for KUAL Booklet variants:

1. Connect your Kindle to your PC.
2. Extract MRPI's `extensions` and `mrpackages` folder to Kindle's visible storage's root. This is where the `document` folder resides.
3. Drop the KUAL files in.
   * Using **KUAL Booklet** or **KUAL Booklet (coplate)**, drop `KUALBooklet_*_install.bin` into `mrpackages` folder.
     * To identify which is which, **Booklet (coplate)** variant will have a commit string in its version number in the file name, such as `KUALBooklet_ff4134d_install.bin`, while **Booklet** will have the version number in its file name, such as `KUALBooklet_v2.7.29_install.bin`.
4. (Optional) Drop any other extensions into the `extensions` folder, and update bins into `mrpackages` folder.
5. Once everything is in place, eject/disconnect your Kindle, then enter `;log mrpi` to start MRPI. `Hush, little baby...` should pop up at the bottom half of the screen.
   * If nothing happens, check and make sure you've placed everything in place correctly.
   * If for whatever reason `;log` doesn't exist, You can still install by dropping `Update_KUALBooklet_hotfix_*_install.bin` into Kindle's visible storage's root, then go into `Settings` > `Update Your Kindle` to install it.
     * Obviously this won't work if your Kindle firmware is too new, and the package hasn't been updated, in which case you'll have to wait for an update.&#x20;

## Once you've completed the steps, feel free to head onto [Disable OTA Updates](optional-disable-ota-updates-on-5.11+.md) for 5.11+ (optional, but recommended), or head to [Installing KOReader](optional-koreader.md) (optional).
