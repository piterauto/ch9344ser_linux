# ch9344 linux serial driver

## Description

​This driver supports USB to quad serial ports chip ch9344 and USB to octal serial ports chip ch348.

## Installation

1. Open `terminal`
2. Clone repository: `git clone https://github.com/piterauto/ch9344ser_linux.git`
3. Change working directory: `cd driver`
4. Compile the driver: `make`
5. Load the driver:
   - Dynamically: `sudo make load` or `sudo insmod ch9344.ko`
   - Permanentelly: `sudo make install`
6. Unload the driver: `sudo make unload` or `sudo rmmod ch9344.ko`
7. To remove driver from system perform `sudo make uninstall`

​If the driver works as intended, the system will create tty devices named `ttyCH9344USBx` in `/dev` directory.

## Important

Before the driver works, you should make sure that the usb device has been plugged in and is working properly, you can use shell command "lsusb" or "dmesg" to confirm that, USB VID of these devices are [1A86], you can view all IDs from the id table which defined in "ch9344.c".

## Note

​In case of any questions you can send message to <tech@wch.cn>.
