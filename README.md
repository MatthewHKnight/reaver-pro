# reaver-pro

Reaver Pro II Firmware and Flashing.

The Reaver Pro II is dead but their are still plenty of vulnerable routers out there in the wild!
I've had these firmware images for a while now I just decided I'd release them.
I offer no support on Reaver Pro.

[![Howto: Unbrick / Reflash Reaver Pro](https://img.youtube.com/vi/s1fg-Gxr-OY/0.jpg)](https://www.youtube.com/watch?v=s1fg-Gxr-OY)

The is almost an hour long reason for I explain a lot of stuff and also I wanted you to see without me editing out parts what you will see in the process of having to flash reaver pro.

Requirements:
Windows 7 Pro - I DO NOT! Recommend a Virtual Machine due to driver issues with the Serial TTL Cable
Serial TTL Cable Buy it here: http://goo.gl/e6DUYz Price: Between $10-13USD Very important you get this exact one!
Phillips Screwdriver

Required files:
Firmware files from github

1 - Reaver Pro Firmware
2 - Stock OpenWRT Firmware - For flashing before you can flash with the Reaver Pro firmware.
3 - PL2303 Prolific Driver - Driver for the Serial TTL Cable.
4 - putty - For accessing serial interface on reaver pro.
DOWNLOAD PUTTY: http://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html
5 - tftpd32 - This is a File server that allows us to send over the OpenWRT firmware via Serial.
DOWNLOAD TFTPD32: http://tftpd32.jounin.net/tftpd32_download.html
6 - Flashing Steps.
7 - An Image of what the Serial Pins look like on Reaver Pro. You need to connect the cables like I say below...

Please note that the PL2303 driver will only work with the Serial TTL Cable from the Google URL Above, If you have a differnet Serial TTL cable then that download that driver.

Connect ONLY!
GND to GND like it shows on the picture.
RXD to the TXD where it shows the TXD in the picture may sound dumb but do it.
TXD to RXD Where it shows the RXD in the picture again I know it sounds dumb but do it.

If you try connecting;
RXD to RXD
and TXD to TXD you will NOT! get a boot message over serial thats why it needs to be in the order I said.

Color of the wires don't matter just make sure you have the right wires going to the right spots on reaver pro and on the serial ttl cable.


Okay!
whatever you do, do not connect the serial ttl cable till after you have install the PL2303 Prolific driver you might need to restart your computer after you install it.

Once you have the Serial TTL driver installed install the TFTPD32

You will also need to setup a static ip by going to the network and sharing area and finding your local area connection and it should be under Change adapter settings on the left assuming you found the local area connection right click on it pick Properties look for TCP/IPv4 highlight it and click the Properties button.

Click: Use the following IP address:
it show allow you to type in the boxes you need to set;
192.168.2.11 for box 1
and then just click box two and it will auto fill in 255 ect..

Be sure to follow the video I cover step by step I'm not gonna sit here typing out the whole process :B

On putty you need to pick;
Serial
and the Speed needs to be:
Speed: 115200
very important that the speed is set to 115200
the COM you need to set as well when you connect the serial TTL go to the device manager on Windows and see what COM the Prolific is set on mine was COM4 but yours might be different.
