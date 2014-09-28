---
layout: post
title:  "Using the Logitech K760 Wireless Solar Keyboard on Windows"
date:   2013-09-08 19:40:00
categories: development
---

**Update:** The application has been converted into a tray application that continously monitors for connect/disconnect signals, and reapplies the fix. Previously, if the keyboard went into stand-by, the application had to be started again to re-fix the F-keys. A new feature has also been added that remaps the previously non-functional eject key to F13. You can then use SharpKeys or similar to remap this key to what you want. [Download]({{ site.url }}/files/WinK760.exe) and replace the executable to try it out.

<img src="/images/k760.png" class="center" />

The K760 is a very nice keyboard made by Logitech. It is clear from the styling, keyboard layout and full name (... for Mac/iPad/iPhone) that it is not made for Windows use, but as it is a standard Bluetooth keyboard it will work *almost* perfectly with any operating system.

There are two fixable issues:

* On the Danish keyboard layout at least, the key between the left shift, and z key is swapped with the key above the tab key.
* The Logitech SetPoint software for Windows does not recognize the keyboard, and it is therefore not possible to read battery status and, more importantly, change how the F-keys function.

The first issue is easily solved using keyboard re-mapping software - I personally like [SharpKeys][]. After installing SharpKeys, SharpKeys will let you type the button you want to change, and what key code should be sent when that button is pressed. After this is done, it should look similar to the image below (with the exception of the caps-lock remapping):

<img src="/images/sharpkeys.png" class="center" style="width: 400px" />

The second issue is quite tricky on the other hand. On Linux, you can use [Solaar][] for most Logitech products, but from looking at the code, it looks like it is Linux only, and only for Logitech devices using the Logitech Unifying Receiver (ie. *not* bluetooth).

Luckily, the protocol used by the K760 is the same as the one used on the K750. The protocol is called HID++ 2.0, and *some* [documentation][HID++2] is available. Through a combination of looking at the Solaar source, and HID++ documentation, I managed to throw together an application that can toggle between F1-12-keys on by default, or function keys on by default.

Source for the application can be found on [Github][WinK760].

**Update:** By request, [a pre-built version of the application]({{ site.url }}/files/WinK760.exe).

[WinK760]: https://github.com/jesperhh/WinK760
[SharpKeys]: http://sharpkeys.codeplex.com/
[Solaar]: https://github.com/pwr/Solaar/
[HID++2]: http://6xq.net/git/lars/lshidpp.git/plain/doc/logitech_hidpp_2.0_specification_draft_2012-06-04.pdf