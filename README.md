# Helm Armbian Image Installation

This repository contains Armbian images for the Helm v2a and Helm v2b devices.  These are the second generation Helms that are square shaped instead of the triangle shaped v1 Helms.  There are two different variants of the Helm v2 and it's important to install the correct image based on the revision of your hardware.  The FCC ID on the label on the bottom of your Helm can be used to determine what version you own.  Generally, but not guaranteed, Helm v2a devices were shipped prior to the Summer of 2022 whereas Helm v2b devices were shipped in the Summer and Fall of 2022.

**Helm v2a**\
FCC ID: 15C-2AYVZ256G\
Latest Arbmian Image: [Armbian_22.11.1-build-38_Helm-v2a_bullseye_legacy_4.4.213_minimal.img](https://github.com/HelmSecure/armbian-images/releases/download/v22.11.1-build-34/Armbian_22.11.1-build-38_Helm-v2a_bullseye_legacy_4.4.213_minimal.img)

**Helm v2b**\
FCC ID: 2AYVZV11256G\
Latest Arbmian Image: [Armbian_22.11.1-build-38_Helm-v2b_bullseye_legacy_4.4.213_minimal.img](https://github.com/HelmSecure/armbian-images/releases/download/v22.11.1-build-34/Armbian_22.11.1-build-38_Helm-v2b_bullseye_legacy_4.4.213_minimal.img)

## Notes
+ Built from Armbian Bullseye release
+ Kernel and u-boot updates provided by Helm Debian Resitory hosted on GitHub
+ Other software package updates provided by Armbian and Debian projects
+ **Linux host PC is required for flashing the image**

## Issues
[Known Issues](https://github.com/HelmSecure/armbian-images/issues)

## Installation Instructions
1. Before installing Armbian on your Helm, backup up any data that you need to preserve.  Once the Arbian image is programmed you will lose access to all data currently stored on your Helm.
2. Helm v2 devices contain a Rockchip rk3399 SoC.  The Rockchip rkdeveloptool running on a Linus host is required to flash the image.  Please following instruction found here for installing the rkdeveloptool on a Linux box.  https://github.com/rockchip-linux/rkdeveloptool
3. Connect your Helm to power and to your router via ethernet
4. When your Helm is fully booted, press and hold the power button for 25 seconds
5. Remove the power cable, press the power button and hold, insert power cable.  Keep the power button pressed for 6 seconds after inserting power and then release.  This process will put your Helm into maskrom mode.
6. Connect to the Helm via a usb-c cable to your Linux host computer using one of the two usb-c ports on the right of the ethernet port when looking at the Helm from the back.
7. Confirm that your Linux host has detected the Helm is maskrom mode.  Running the lsusb command on the Linux host should show a device named "Fuzhou Rockchip Electronics Company RK3399 in Mask ROM mode".  If the device doesn't show, attempt steps 4-6 again.
8. Flash the image to your Helm using these commands:

```
$ sudo rkdeveloptool db helm-loader-build-38.bin
$ sudo rkdeveloptool wl 0 [the .img file downloaded from here]
$ sudo rkdeveloptool ul helm-loader-build-38.bin
$ sudo rkdeveloptool rd
```


## Armbian Instructions
+ To setup Armbian after flashing you will need to connect to your Helm over your network using SSH.  Please see instructions from Armbian about connecting via ssh for the initial setup: https://docs.armbian.com/User-Guide_Getting-Started/#how-to-login
