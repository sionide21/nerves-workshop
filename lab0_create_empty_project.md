Creating a nerves project
=========================

## Generate project

```
mix nerves.new pizero_blinkenlight
cd pizero_blinkenlight
```

## Compile for the Raspberry Pi Zero target

```
MIX_TARGET=rpi0 mix deps.get
MIX_TARGET=rpi0 mix firmware
```

## Burn to SD card

Plug SD card into reader

```
MIX_TARGET=rpi0 mix firmware.burn
```

Will prompt if it's the correct device (should be something like "7.42 GiB memory card")

Say yes and it will prompt for password and burn card.

## Boot device

Plug usb cable into micro usb port labeled "USB", it's the one closer to the center of the board.

Hook up to computer and wait about 2 seconds.

## Connect to IEx over serial console

* [Mac Instructions](console/mac.md)
* [Linux Instructions](console/linux.md)
