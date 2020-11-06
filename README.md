# test GoPro camera

This is just a test script to access GoPro camera and using OpenCV to display the frames.

The GoPro camera API can be from https://github.com/KonradIT/gopro-py-api . This is not an official API from GoPro, but the developers there are doing a very nice API for us to help controlling GoPro to do some automation stuff.

Make sure you install their latest API, at the time I am writing this, it's 4.1.0, so please so `pip install goprocam==4.1.0` before using it.

## My test scripts

`streamGoPro.py` will need the GoPro Wifi to be turned on, this is quite not useful because you need a mobile phone and GoPro app to enable GoPro wifi first (I am using GoPro HERO7 and 9, and this step is needed, let me know how's the other version). The code is pretty much comes from this guy https://youtu.be/Wi6aMYFSwcA , but I was playing around and modified a bit.

`testGoProUSB.py` is to use GoPro as webcam, your PC will join the GoPro network from USB, so make sure your ethernet interface name is correct before using (mine is enp0s20f0u4). Or you can specify the ip_address instread, when connecting with USB-C cable, the ip_address of the GoPro is different from Wifi mode, so with USB-C it is `ip_address="172.26.174.51"`. Make sure your GoPro is in "GoPro Connect" when USB is plugging. 