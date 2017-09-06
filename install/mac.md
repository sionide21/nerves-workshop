Mac Installation Instructions
=============================

## Install fwup requirements

```
brew install fwup squashfs coreutils
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
