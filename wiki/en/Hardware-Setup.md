---
layout: wiki
title: "Hardware Setup"
lang: "en"
permalink: "/wiki/Hardware-Setup"
---

{% include breadcrumb.html root="Using Jamulus" branch1="Getting Started" branch1-url="Getting-Started" %}

# Hardware Setup

## General info

**For Jamulus to run stable it is recommended to use a PC with at least 1.5 GHz CPU frequency.**

**Windows users**: You need to install an ASIO driver. A sound card with a native ASIO driver is recommended. Have a look at the [Windows installation page](Installation-for-Windows) for further information.

## Example Setups

Setting up hardware usually boils down to 4 points, although each setup is different.

1. Plug the interface into a USB port on your computer
2. Close all programs and start Jamulus (don't forget to choose the right inputs in Jamulus's settings)
3. Plug in your instrument/microphone and headphones
4. Connect to a Jamulus server and have fun!


## Windows: Audio interface connection - ASIO4ALL

This is an example Windows client installation with the [Behringer U-CONTROL UCA202](https://www.amazon.com/Behringer-U-Phono-UFO202-Audiophile-Interface/dp/B002GHBYZ0) audio device.
The following instructions might be similar with other audio devices.

_**The exact method of connecting your instrument will of course vary depending on your hardware.**_

#### 1. Plug the interface into a USB port on your computer

In future, always use the same USB port for the audio device.

**Windows users**: If not already done: download and install the [free ASIO sound driver (ASIO4ALL)](https://www.asio4all.org){: target="_blank" rel="noopener noreferrer"}. Some people have also reported success using [this ASIO native driver](http://www.behringerdownload.de/_software/BEHRINGER_2902_X64_2.8.40.zip){: target="_blank" rel="noopener noreferrer"} __currently not available__, although it's not listed on Behringer's product pages as of April 2020.


#### 2. Start Jamulus

Configure Jamulus to use the correct sound setup (see [this excellent guide](https://www.facebook.com/notes/jamulus-online-musicianssingers-jamming/idiots-guide-to-jamulus-app/510044532903831/) by [Simon Tomlinson](https://www.facebook.com/simon.james.tomlinson?eid=ARBQoY3KcZAtS3pGdLJuqvQTeRSOo4gHdQZT7nNzOt1oPMGgZ4_3GERe-rOyH5PxsSHVYYXjWwcqd71a) on Facebook).

Make sure you have switched off the monitor button on your Behringer U-CONTROL UCA202 (otherwise you will hear both the original sound you are sending to the Jamulus server as well as the returning sound, and may get feedback).

#### 3. Plug in your instrument and headphones

Connect your instrument to the input socket of the Behringer U-CONTROL UCA202. Plug your headphones into the Behringer U-CONTROL UCA202.

#### 4. Connect to a Jamulus server.

You're done! Have fun!

## Linux: Audio interface connection with QjackCtl

Refer to the Linux [client install guide](Installation-for-Linux#configure-jack-with-qjackctl).

## Linux: Low Latency Kernels for Jamulus

You might want to install [Ubuntu Studio](https://ubuntustudio.org/). It adds a second option in your boot menu for a low-latency kernel. The key to successful jamming is "low latency" between servers and connected Jamulus clients. If the underlying Linux system is started with a low-latency kernel then it has a positive impact on latency for your Jamulus sessions.


## Points to note about inputs

- If you want to connect 2 or more sources (e.g. voice + synth + guitar), it is important to note that Jamulus currently handles only 2 input channels (L/R). So the hardware being used must provide a mixed-down stereo output to Jamulus. Alternatively, run two instances of Jamulus, if your hardware supports it, or use virtual audio inputs to Jamulus for each hardware input.
- Audio interfaces generally output a mixed signal on their analogue output, but separate signals (1 per source) on their digital output (USB/FireWire/Thunderbolt).
- Mixers generally only output mixed-down signals on their analogue output.
- Mixers with USB/FireWire/Thunderbolt generally output a mixed-down signal on their **analogue** output AND separate signals only (no mixed-down signal) on their **digital** output.
- A few Mixers with USB/FireWire/Thunderbolt will either send **only** a mixed-down signal to the **digital** output (small/budget mixers), or else also ADD a stereo mixed-down signal to the separate signals on the digital output.

_(Thanks to [pcar75](https://github.com/pcar75) for this information)_

## Other examples

**This video documents a [live jam session](https://youtu.be/c8838jS2g3U).** I am using a Lexicon Omega USB audio card on a 2009 Mac Mini. My bandmates all use Windows 10 and have Behringer audio cards, e.g. the Behringer Xenyx 1204USB. My internet connection is 10 Mbit/s down / 1 Mbit/s upstream via DSL.

**Jamulus user [Andrew Evans](https://sourceforge.net/u/belvario/profile/)**: With bandmates all within one city (but spanning 2 ISPs) and achieving a consistent 20 ms ping time, running the server on a separate dedicated Windows machine and a client on a MacBook Pro. Remote players on MacBook Air. Everyone on wired Ethernet connections to their home router/gateways. We used WhatsApp video to see each other (with audio muted - it's funny to see how far behind the WhatsApp audio lags from Jamulus though!)

## Having problems?

Please see the [Client Troubleshooting FAQ](Client-Troubleshooting)
