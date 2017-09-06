Setup networking
================

## Add nerves_network dependency

* Open `mix.exs`
* Find `def deps(target) do` section
* Add `{:nerves_network, "~> 0.3"},` to the list
* Fetch dependencies with `MIX_TARGET=rpi0 mix deps.get`

## Configure regulatory domain

* Open `config/config.exs`
* Add the following settings:

```
config :nerves_network,
  regulatory_domain: "US"
```

## Recompile and burn new firmware

```
MIX_TARGET=rpi0 mix firmware
MIX_TARGET=rpi0 mix firmware.burn
```

## Connect to IEx over serial console

* [Mac Instructions](console/mac.md)
* [Linux Instructions](console/linux.md)

## Connect to network

```
Nerves.Network.setup "wlan0", ssid: "TechSquare Labs", key_mgmt: :"WPA-PSK", psk: "<password>"
```

## Test connection

```
{:ok, sock} = :gen_tcp.connect('twitter.moosen.net', 7777, active: true, packet: :line)
:gen_tcp.send(sock, "debug test\n")
flush()
```
