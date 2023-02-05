---
description: >-
  This page will guide you through how to make the Kindle Voyage run firmware
  5.14+, Keep in mind that this is experimental, and you may damage your device.
---

# Forcing KV to run 5.14+

Info taken from the original thread: [https://www.mobileread.com/forums/showthread.php?t=343385](https://www.mobileread.com/forums/showthread.php?t=343385)

So, the PW3 and the KV is actually almost identical in terms of the underlying hardware, and with an identical partition layout, it is possible to cross-flash firmware from one device to another. Heck, [even the KT2 with 256MB of ram can run 5.14+](https://www.reddit.com/r/kindle/comments/qvgerd/teaching\_old\_dogs\_new\_tricks\_newest\_update/) though it is not really recommended as the React UI of 5.13.7+ does take up more resources and memory exhaustion becomes a problem.

The only real exception to this Wario hardware family (PW2, PW3, KT2, KV) is the PW2 as it has a slightly smaller RootFS than the other 3 ([as I've found out the hard way](https://www.mobileread.com/forums/showthread.php?t=348801)), while it is still possible to run 5.14.1 on the PW2, some modifications are needed to trim down the RootFS' size.

## By following this guide, I bear no responsibility if you break your Kindle, caused a house fire, or accidentally open up a wormhole to the 818th dimension. You have been warned!



## Prerequisites:

* A Kindle Voyage (duh) with a 1.8v USB to serial adapter soldered to it.
* A PC running Linux, or a Mac.&#x20;
* NiLuJe's [KindleTool](https://github.com/NiLuJe/KindleTool). (Grab this from your distro's package manager, or `brew` in macOS.)
* PW3 update file, [https://s3.amazonaws.com/firmwaredownloads/update\_kindle\_all\_new\_paperwhite\_5.XX.X.bin](https://s3.amazonaws.com/firmwaredownloads/update\_kindle\_all\_new\_paperwhite\_5.XX.X.bin)\
  Replace `5.XX.X` with the version you desire, such as `5.14.2`.

## Process:

1. Download the copy of a PW3 update file as mentioned above. Then extract it using KindleTool:

```
kindletool extract ~/Downloads/update_kindle_all_new_paperwhite_5.XX.X.bin /tmp/pw3
```

2. Once that's done, decompress `rootfs.img.gz` to obtain the raw `rootfs.img`:

```
gzip -d /tmp/pw3/rootfs.img.gz
```

3. Reboot your Kindle with active serial connection, then interrupt the boot process by rapidly hitting Enter until you get to the `uboot` prompt. Then boot into `DIAGS` mode:

```
uboot > bootm 0xE41000
```

4. Once you're in `DIAGS`, export the userspace partition:

```
usb export
```

5. Transfer `rootfs.img` to the device.
6. Eject the Kindle from the host PC and exit USB Export mode.

```
x   ICE-WARIO-WFO-512 - USB EXPORT -  71
   ~~~~  1.16.614.264341  ~~~~ 
     pcbId:04XXXXXXXXXXXX
   USB device exported
    
   Once you are done
   Eject the USB device from the PC then
 
 
   Battery capacity  71
 
(Q)-to continue  
 
(X)-Exit
x
```

7. Exit diags mode, then drop to a shell.

```
exit login
```

8. Flash `rootfs.img` using ~~Disk Destroyer~~ DD, this will take a while to complete:

```
[root@[192_168_15_244] root]# dd if=/mnt/us/rootfs.img of=/dev/mmcblk0p1 bs=4096
112500+0 records in
112500+0 records out
460800000 bytes (439.5MB) copied, 95.986967 seconds, 4.6MB/s
```

9. Reboot the device. It will now boot into the firmware you installed.

```
reboot
```



## Once you've confirmed that everything works as it should, have fun with your Paperwhite 3 Voyage Edition!
