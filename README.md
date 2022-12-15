# armbian-images

This repository contains Armbian images for the Helm v2a and Helm v2b devices.  These are the second generation Helms that are square shaped instead of the triangle shaped v1 Helms.  There are two different variants of the Helm v2 and it's important to make sure to install the correct image based on the revision of your hardware.  The FCC ID on the label on the bottom of your Helm can be used to determine what version you own.  Generally, but not guaranteed, Helm v2a devices were shipped prior to the Summer of 2022 whereas Helm v2b devices were shipped in the Summer and Fall of 2022.

**Helm v2a**\
FCC ID: 15C-2AYVZ256G\
Latest Arbmian Image: [Armbian_22.11.1-build-34_Helm-v2a_bullseye_legacy_4.4.213_minimal.img](https://github.com/HelmSecure/armbian-images/releases/download/v22.11.1-build-34/Armbian_22.11.1-build-34_Helm-v2a_bullseye_legacy_4.4.213_minimal.img)

**Helm v2b**\
FCC ID: 2AYVZV11256G\
Latest Arbmian Image: [Armbian_22.11.1-build-34_Helm-v2b_bullseye_legacy_4.4.213_minimal.img](https://github.com/HelmSecure/armbian-images/releases/download/v22.11.1-build-34/Armbian_22.11.1-build-34_Helm-v2b_bullseye_legacy_4.4.213_minimal.img)

## Notes
+ Built from Armbian Bulleye release
+ Kernel and u-boot updates provided by Helm Debian Resitory hosted on GitHub
+ Other software package updates provided by Armbian and Debian projects

## Issues
[Known Issues](https://github.com/HelmSecure/armbian-images/issues)

## Installation Instructions
1. Before installing Armbian on your Helm make sure that you've backed up any data that you need to preserve.  Once the Arbian image is programmed you will lose access to all data currently stored on your Helm.
2. Helm v2 devices contain Rockchip rk3399 processors and so Rockchip tools are required to install the firmware.
