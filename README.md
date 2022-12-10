# armbian-images

This repository contains Armbian images for the Helm v2a and Helm v2b devices.  These are the second generation Helms that are square shaped instead of the triangle shaped v1 Helms.  There are two different variants of the Helmv v2 and it's important to make sure to install the correct image based on the revision of your hardware.  The serial number of your Helm which is found on sticker on the bottom can be used to determine what variant you have.  Generally, but not guaranteed, Helm v2a devices were shipped prior to the Summer of 2022 whereas Helm v2b devices were shipped in the summer and fall of 2022.

Helm v2a Serial Numbers


Helm v2b Serial Numbers



## Installation Instruction
1) Before installing Armbian on your Helm make sure that you've backed up any data that you need to preserve.  Once the Arbian image is programmed you will loose access to any of the data currently stored on your Helm.
2) Helm v2 devices contain Rockchip rk3399 processors and so Rockchip tools are required to install the firmware.
