Blinking a light
================

## Add nerves_leds dependency

* Open `mix.exs`
* Find `def deps(target) do` section
* Add `{:nerves_leds, "~> 0.8.0"}` to the list
* Fetch dependencies with `MIX_TARGET=rpi0 mix deps.get`

## Recompile and burn new firmware

```
MIX_TARGET=rpi0 mix firmware
MIX_TARGET=rpi0 mix firmware.burn
```

## Connect to IEx over serial console

* [Mac Instructions](console/mac.md)
* [Linux Instructions](console/linux.md)

## Control Light

```
# Quirk of the rpi0: false is on, true is off
Nerves.Leds.set("led0", true)
Nerves.Leds.set("led0", false)
```
