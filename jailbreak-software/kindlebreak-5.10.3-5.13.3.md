---
description: >-
  This page will guide you through on how to use KindleBreak to Jailbreak your
  Kindle that's on firmware 5.10.3-5.13.3... with some exceptions.
---

# KindleBreak (5.10.3-5.13.3\*)

Info taken from the original thread: [https://www.mobileread.com/forums/showthread.php?t=338268](https://www.mobileread.com/forums/showthread.php?t=338268)

Before we get started, there's a few exceptions with the firmware it supports. Most notably, on the KT2 and PW2 (6th generation hardware), there was a firmware update `5.12.2.2` which patches the exploit KindleBreak uses, in which case you should be using [WatchThis](watchthis-5.12.2.2-5.13.4-5.14.2.md) instead.

_TL;DR of this jailbreak: Download the zip, copy the files to the top level storage of your Kindle, go to `file:///mnt/us/kindlebreak.html`, wait for it to restart then go to_ [_Post Jailbreak_](broken-reference)_._



## Prerequisites:

Here is a table on which models are supported, and what firmware versions are supported. Unlike WatchThis, any models with any versions on this table will be supported.

| Models                                                                                                                             | Firmware Version                                                                                                                                                                                                                                     |
| ---------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <ul><li>KOA3</li><li>KT4</li><li>PW4</li><li>KOA2</li><li>KT3</li><li>KOA</li><li>KV</li><li>PW3</li><li>KT2</li><li>PW2</li></ul> | <ul><li>5.13.3</li><li>5.13.2</li><li>5.13.1</li><li>5.12.5</li><li>5.12.4</li><li>5.12.3</li><li>5.12.2.1.1</li><li>5.12.2.1</li><li>5.12.2</li><li>5.12.1.1</li><li>5.12.1</li><li>5.11.2</li><li>5.11.1.1</li><li>5.11.1</li><li>5.10.3</li></ul> |

#### Versions that won't work with KindleBreak:

* Anything newer than 5.13.3, in which case you should use [WatchThis (5.13.4-5.14.2)](watchthis-5.12.2.2-5.13.4-5.14.2.md) instead.
* 5.12.2.2, despite the name, this version is actually newer than 5.13.3. Use [WatchThis](watchthis-5.12.2.2-5.13.4-5.14.2.md) instead.
* Anything older than 5.10.3.



## If you've determined that KindleBreak supports your device/firmware version:

1. Download [jb-kindlebreak.zip](https://storage.gra.cloud.ovh.net/v1/AUTH\_2ac4bfee353948ec8ea7fd1710574097/mr-public/Touch/jb-kindlebreak.zip) (MD5: 0215C36CC1E3AD8136A67DAEBE369452)
2. Unzip, now there should be these files:
   * jb
   * jb.sh
   * kindlebreak.html
   * kindlebreak.jxr
3.  Connect your Kindle to your computer, then copy the 4 files above to the root of your Kindle's storage (where the `documents` folder is.)

    <figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption><p>It should look something like this.</p></figcaption></figure>
4. Eject and unplug your Kindle.
5.  Go to the Experimental Browser from the top right menu, then navigate to&#x20;

    ```
    file:///mnt/us/kindlebreak.html
    ```

    \
    (Make sure that it is `file:///` and not `file://`)
6. Your browser should **freeze, crash** and after some time (this can range from few seconds to several minutes depending on your device) **your Kindle will reboot.** It'll probably give you some kind of error window with the title along the lines of "**Application Error**" or "**Collecting Debug Info**".

## Once your device has rebooted, you're finished with the tutorial. Head onto [Post Jailbreak](broken-reference) section to finish setting up things.

