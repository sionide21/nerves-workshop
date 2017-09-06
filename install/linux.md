Linux Installation Instructions
===============================

## Install fwup requirements

```
sudo apt-get install ssh-askpass squashfs-tools
```


## Install fwup

```
wget https://github.com/fhunleth/fwup/releases/download/v0.15.4/fwup_0.15.4_amd64.deb
sudo dpkg -i fwup_0.15.4_amd64.deb
```

## Update hex and rebar

```
mix local.hex
mix local.rebar
```

## Install nerves archive

```
mix archive.install https://github.com/nerves-project/archives/raw/master/nerves_bootstrap.ez
```
