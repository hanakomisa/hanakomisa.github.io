---
description: >-
  This page will guide you through setting up a Hotfix, so that it auto-applies
  the jailbreak if a software update occurs.
---

# Set up a Hotfix

_The instructions currently slightly differ if you have used WatchThis to jailbreak your Kindle. The guide will have two separate tabs to cover the difference._

{% tabs %}
{% tab title="Normal Hotfix" %}
1. Download "K5 JailBreak Hotfix" from [NiLuJe's snapshot thread](https://www.mobileread.com/forums/showthread.php?t=225030).
2. Connect the device to a PC and copy `Update_jailbreak_hotfix_1.16.N_install.bin` to the root of the Kindle storage, then disconnect the device.
   * _In the case of it throwing an invalid update error upon unplugging, it means the hotfix package hasn't been updated for that version yet. In which case you'll just have to wait_.
3. Go to **Settings** > **Update Your Kindle** to install the update.
{% endtab %}

{% tab title="WatchThis Hotfix" %}
1. After the device has rebooted, type `;uzb` into the search bar. (This will enable the USBMS protocol since demo mode has that disabled by default.)
2. Connect the device to a PC and copy `update_hotfix_watchthis_custom.bin` to the root of the Kindle storage.
3. Eject the device and either enter `;dsts` or swipe down and select the settings icon to enter the device settings menu.
4. Select **Update Your Kindle** to install the custom hotfix.
5. This will take your device out of demo mode, rebuild the application registry and clean up unneeded jailbreak files.
{% endtab %}
{% endtabs %}

## Once you've installed the Hotfix, continue to [Installing KUAL/MRPI](installing-kual-mrpi.md).
