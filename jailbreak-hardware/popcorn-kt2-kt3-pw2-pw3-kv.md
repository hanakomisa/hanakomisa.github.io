---
description: >-
  This page will guide you through how to use Popcorn to jailbreak your Kindle.
  This is a method that requires you to open up your Kindle, be careful with
  those razor blades and tweezers!
---

# Popcorn (KT2, KT3, PW2, PW3, KV)

Info taken from original thread: [https://www.mobileread.com/forums/showthread.php?t=345655](https://www.mobileread.com/forums/showthread.php?t=345655)

A small note before we start, the Kindle Voyage is fully covered by both [KindleBreak](../jailbreak-software/kindlebreak-5.10.3-5.13.3.md) and [WatchThis](../jailbreak-software/watchthis-5.12.2.2-5.13.4-5.14.2.md) so if you don't feel like pulling apart your precious Voyage, use that instead!

## Prerequisites:

* a PC running Linux or Windows (instructions will differ.)
  * In case of Linux, `imx_usb_loader`.
* A paperclip, jumper cable or tweezers.
* The knowledge to open up your Kindle without breaking it.
* Steady hands, wouldn't want to short 3.3v to GND now would you?

## Preparation:

To use this jailbreak, you will need to open up your device, attach your device to your host PC using a USB cable and activate SDP mode. There's a number of ways that you can do this, with some being easier than others.

### Without removing PCB (KT2, KT3, PW2, PW3 only):

{% tabs %}
{% tab title="KT2" %}
Refer to this image. ([Credit](https://www.mobileread.com/forums/showthread.php?t=340387))

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption><p>Connect these two points together.</p></figcaption></figure>
{% endtab %}

{% tab title="KT3" %}
Refer to this image. ([Credit](https://www.mobileread.com/forums/showthread.php?t=327055))

<figure><img src="../.gitbook/assets/image (4).png" alt=""><figcaption><p>Connect these two points together on KT3's motherboard.</p></figcaption></figure>
{% endtab %}

{% tab title="PW2/PW3" %}
Connect the right side (rectangle pad) of CR501 to a 3.3V source such as TP508.

<figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>
{% endtab %}
{% endtabs %}

### After removing the PCB:

_Removing the PCB is only necessary for the Kindle Voyage to use this Jailbreak. As always I recommend having_ [_iFixit's Kindle Voyage Teardown_](https://www.ifixit.com/Teardown/Kindle+Voyage+Teardown/32278) _open to get a general idea on what to do._

{% tabs %}
{% tab title="KV" %}
Connect TM500 to TM501 then reset the device.

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption><p>might have to pull out the soldering iron for this one...</p></figcaption></figure>
{% endtab %}

{% tab title="KT2, PW2, PW3" %}
Connect TP1706 to TP401, then reset the device.
{% endtab %}
{% endtabs %}

TL;DR: Connect the Kindle to your PC, Short those points, reboot your Kindle by holding the power button for around 15 seconds while those points are connected, then it should be in SDP mode ready for the Jailbreak to be initialized.

## The Jailbreak:

{% tabs %}
{% tab title="Linux" %}
If you've done it correctly, you should see something like this when you run `dmesg` on your PC:

```
[ 2470.327595] usb 1-13: new high-speed USB device number 7 using xhci_hcd
[ 2470.476311] usb 1-13: New USB device found, idVendor=15a2, idProduct=0063, bcdDevice= 0.01
[ 2470.476319] usb 1-13: New USB device strings: Mfr=1, Product=2, SerialNumber=0
[ 2470.476324] usb 1-13: Product: SE Blank MEGREZ
[ 2470.476327] usb 1-13: Manufacturer: Freescale SemiConductor Inc 
[ 2470.478445] hid-generic 0003:15A2:0063.0008: hiddev1,hidraw4: USB HID v1.10 Device [Freescale SemiConductor Inc  SE Blank MEGREZ] on usb-0000:00:14.0-13/input0
```

To run the jailbreak, extract [the jailbreak](https://www.mobileread.com/forums/attachment.php?attachmentid=198921\&d=1673376193) to a convenient location on your PC, open a terminal, and run the relevant command for your device.

```
# For PW2, PW3, KT2, KV
sudo imx_usb -c imx_usb_loader/wario
# For KT3
sudo imx_usb -c imx_usb_loader/heisenberg
```
{% endtab %}

{% tab title="Windows" %}
Before we get started:

Download this for PW2, PW3, KT2, KV: [https://www.mobileread.com/forums/showpost.php?p=4217167\&postcount=17](https://www.mobileread.com/forums/showpost.php?p=4217167\&postcount=17)

Download this for KT3: [https://www.mobileread.com/forums/showpost.php?p=4288479\&postcount=60](https://www.mobileread.com/forums/showpost.php?p=4288479\&postcount=60)



Once you've unarchived the package, activate SDP mode on your Kindle as instructed above, open `MFGTool.exe` and click `Start`. Everything should work.
{% endtab %}
{% endtabs %}

## Once the jailbreak has finished, the device will reboot, then you can proceed to [Installing KUAL/MRPI](../post-jailbreak/installing-kual-mrpi.md).
