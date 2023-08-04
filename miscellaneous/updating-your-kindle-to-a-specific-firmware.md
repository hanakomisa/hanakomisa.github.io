---
description: >-
  This page will guide you through how to download a specific firmware version
  for your Kindle.
---

# Updating your Kindle to a specific Firmware

Info taken from original thread: [https://www.mobileread.com/forums/showthread.php?t=338268](https://www.mobileread.com/forums/showthread.php?t=338268)

## <mark style="color:red;">Notice: Firmware 5.15.1.1 has introduced some breaking changes. DO NOT UPDATE PAST 5.15.1.</mark>

Recently, Basti564 (their [Fediverse](https://wetdry.world/@basti564) | [Twitter](https://twitter.com/Basti564) | [YouTube](https://www.youtube.com/@Basti564)) has backed up all the Kindle firmware versions that is still available on Amazon's servers, and have put them up on their archive page, https://cocaine.trade (lovely url btw <3)&#x20;

{% tabs %}
{% tab title="Community Archive (cocaine.trade)" %}
* Visit [https://files.cocaine.trade/firmware/kindle/](https://files.cocaine.trade/firmware/kindle/) to grab your firmware. As of writing, it includes all of the non-legacy (KT2/PW2 and newer) firmwares up to 5.16.x (current latest), as well as legacy 5.x devices such as the KT and PW1.
  * For your own interest, if you're planning to keep the jailbreak, I recommend you stay on 5.14.2 or below, unless if you have access to [Popcorn](../jailbreak-hardware/popcorn-kt2-kt3-pw2-pw3-kv.md) or Serial method. While the jailbreak can work on newer versions provided you did not factory reset and have let the JB bridge initialize correctly (or reapplied with a hotfix after upgrade), if something happens to your install and you have to reflash your Kindle, you won't be able to rejailbreak.
{% endtab %}

{% tab title="Amazon's Own Server" %}
Amazon, at least as for now, has not deleted previous versions of their firmware files. So it is possible to just grab a link for yourself, edit the version number, then download the version you desired. This might be useful if you have had a Kindle laying around for a while with a dead battery and it's on a very old version of the firmware, or if you're trying to [downgrade your Kindle](downgrading-your-kindle-firmware.md).

*   Choose your device from the list below, copy the URL displayed next to its nickname and replace 5.XX.X with your desired firmware version. Make sure that the firmware you chose is on the list of supported versions above! PW2 and KT2 don't have firmware above `5.12.2.2`, you won't be able to download them. PW5 starts at `5.14.1.1`, the KT5 starts at `5.15.1` and the Kindle Scribe starts at `5.16.1`.



    * PW2: [https://s3.amazonaws.com/firmwaredownloads/update\_kindle\_paperwhite\_v2\_5.XX.X.bin](https://s3.amazonaws.com/firmwaredownloads/update\_kindle\_paperwhite\_v2\_5.XX.X.bin)
    * KT2: [https://s3.amazonaws.com/firmwaredownloads/update\_kindle\_5.XX.X.bin](https://s3.amazonaws.com/firmwaredownloads/update\_kindle\_5.XX.X.bin)
    * PW3: [https://s3.amazonaws.com/firmwaredownloads/update\_kindle\_all\_new\_paperwhite\_5.XX.X.bin](https://s3.amazonaws.com/firmwaredownloads/update\_kindle\_all\_new\_paperwhite\_5.XX.X.bin)
    * KV: [https://s3.amazonaws.com/firmwaredownloads/update\_kindle\_voyage\_5.XX.X.bin](https://s3.amazonaws.com/firmwaredownloads/update\_kindle\_voyage\_5.XX.X.bin)
    * KOA: [https://s3.amazonaws.com/firmwaredownloads/update\_kindle\_oasis\_5.XX.X.bin](https://s3.amazonaws.com/firmwaredownloads/update\_kindle\_oasis\_5.XX.X.bin)
    * KT3: [https://s3.amazonaws.com/firmwaredownloads/update\_kindle\_8th\_5.XX.X.bin](https://s3.amazonaws.com/firmwaredownloads/update\_kindle\_8th\_5.XX.X.bin)
    * KOA2: [https://s3.amazonaws.com/firmwaredownloads/update\_kindle\_all\_new\_oasis\_5.XX.X.bin](https://s3.amazonaws.com/firmwaredownloads/update\_kindle\_all\_new\_oasis\_5.XX.X.bin)
    * PW4: [https://s3.amazonaws.com/firmwaredownloads/update\_kindle\_all\_new\_paperwhite\_v2\_5.XX.X.bin](https://s3.amazonaws.com/firmwaredownloads/update\_kindle\_all\_new\_paperwhite\_v2\_5.XX.X.bin)
    * KT4: [https://s3.amazonaws.com/firmwaredownloads/update\_kindle\_10th\_5.XX.X.bin](https://s3.amazonaws.com/firmwaredownloads/update\_kindle\_10th\_5.XX.X.bin)
    * KOA3: [https://s3.amazonaws.com/firmwaredownloads/update\_kindle\_all\_new\_oasis\_v2\_5.XX.X.bin](https://s3.amazonaws.com/firmwaredownloads/update\_kindle\_all\_new\_oasis\_v2\_5.XX.X.bin)
    * PW5: [https://s3.amazonaws.com/firmwaredownloads/update\_kindle\_all\_new\_paperwhite\_11th\_5.XX.X.bin](https://s3.amazonaws.com/firmwaredownloads/update\_kindle\_all\_new\_oasis\_v2\_5.XX.X.bin)
    * KT5: [https://s3.amazonaws.com/firmwaredownloads/update\_kindle\_11th\_5.XX.X.bin](https://s3.amazonaws.com/firmwaredownloads/update\_kindle\_11th\_5.15.1.bin)
    * KS: [https://firmwaredownloads.s3.amazonaws.com/update\_kindle\_scribe\_5.XX.X.bin](https://firmwaredownloads.s3.amazonaws.com/update\_kindle\_scribe\_5.16.1.bin)

    \

{% endtab %}
{% endtabs %}

Once you have the firmware version you desire, do the following:

1. Connect your kindle to your PC with an USB in USBMS mode and put the downloaded `update_kindle_*.bin` file to the top-level/root of the visible USB storage. (It's the same directory where the documents folder is.)\
   \

2. Unplug your USB, go to Settings on your Kindle, then from the top right menu, choose Update Your Kindle. Your kindle will restart and update to the new firmware version.
