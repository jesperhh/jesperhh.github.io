---
layout: post
title:  "Silent PC Build"
date:   2014-09-28 19:30:00
categories: hardware
---

My previous pc was from 2007, and was getting a bit old, even with upgrades (SSD, new GPU and additional memory). When the first passive NVIDIA GTX 750 Ti arrived, I decided it was time to upgrade. See below for parts list and my comments.

### Parts

<img src="/images/parts.jpg" class="center" />

* **Processor**: Intel® Core™ i7-4790K Processor (8M Cache, up to 4.40 GHz)
* **Motherboard**: Asus Z97M-PLUS
* **Memory**: 2 x Crucial DDR3 BallistiX Tactical 16GB
* **Case**:Fractal Design Define Mini MicroATX Tower
* **Graphics**: Palit GeForce® GTX 750 Ti KalmX (2048MB GDDR5)
* **Power supply**: Seasonic Platinum-520 Fanless
* **Storage**: Samsung 840 PRO (250 GB) and Samsung 840 EVO SSD (500 GB)
* **CPU Cooler**: Noctua NH-U12S
* **Additional Cooling**: <del>2</del> 1 Scythe GentleTyphoon 120 mm

### Comments on the build
* The 4790K is a huge upgrade over the Intel Q6600 quad core in the previous build.
* The motherboard is nice looking and works well, but I do not understand why they only included 2 fan headers (in addition to the CPU fan header). I solved the issue with a simple splitter cable (StarTech TX3 Fan Power Splitter Cable), but it appears that this can cause issues when you connect two different fan types to the same header. In addition, I have not yet been able to control the fans through Speedfan, and Asus' AI Suite 3 cannot control fans based on GPU temperature.
* The Define Mini case is very nice - it is lower than the previous Antec P182, but not slimmer. I did have a few issues with it; the biggest was that the hard drive mounting was much worse at eliminating vibration than the P182. This may have been me mounting the disk in a wrong way, but in the end, I just gave up, bought an additional SSD and chucked the old spinning disk. The second issue was that I could not fit a long power supply and use the bottom fan slot as well, but there is ample airflow without it.
* The GPU was the biggest upgrade - not in terms of performance, but noise reduction. Based on benchmarks, the old Asus NVIDIA 560 TI should be a relatively quiet card, but when under load, the fan noise was VERY annoying. The Palit 750 Ti KalmX is as far as I know the fastest fanless card out there right now, and so far, it has handled the games I have thrown at it nicely (Mass Effect 3 and Borderlands 2). The only issue is that the software that comes with the card is quite bad (Palit Thunder Master) - I simply cannot get it to persist an overclock over reboots.
* The Noctua cooler fits well inside the case and with the motherboard. It handles that heat from the 4790K without issues - when idle I get temperatures around 43 °C at 220 RPM.

Overall, I am very happy with the build and the noise level. The only time I hear it is before the BIOS is loaded and the fans are running at 100% RPM, and even then it is almost inaudible.