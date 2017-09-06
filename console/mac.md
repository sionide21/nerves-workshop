Mac Connect to Console
======================

Device name will be in the format `/dev/tty.usbmodemNNNN`.
Find it by running `ls /dev/tty.usbmodem*`

If more than one device shows up:

* unplug the rpi0
* run `ls /dev/tty.usbmodem*`
* plug back in the rpi0
* run `ls /dev/tty.usbmodem*` again
* it will be the one that wasn't in the first listing

```
screen /dev/tty.usbmodemNNNN 115200
```
