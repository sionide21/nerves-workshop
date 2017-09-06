Linux Connect to Console
========================

To access serial ports, you have to add yourself to the `dialout` group
```
sudo usermod -a -G dialout $USER
```

Device name will be in the format `/dev/ttyACM...` or `/dev/ttyUSB...`.
Find it by running `ls /dev/tty[AU]*`

If more than one device shows up:

* unplug the rpi0
* run `ls /dev/tty[AU]*`
* plug back in the rpi0
* run `ls /dev/tty[AU]*` again
* it will be the one that wasn't in the first listing

```
screen /dev/tty... 115200
```
