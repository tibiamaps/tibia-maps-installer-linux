# Tibia maps installer for Linux [![Build status](https://travis-ci.org/tibiamaps/tibia-maps-installer-linux.svg)](https://travis-ci.org/tibiamaps/tibia-maps-installer-linux)

`install-tibia-maps` is a Bash script that downloads the latest version of the `Automap` data provided by [the tibia-map-data project](https://github.com/tibiamaps/tibia-map-data) and extracts it to the `~/.tibia/Automap` folder.

## Installation

Store this script locally and run it again every now and then to update your maps to the latest version.

```sh
curl https://raw.githubusercontent.com/tibiamaps/tibia-maps-installer-linux/master/install-tibia-maps > ~/bin/install-tibia-maps; chmod +x ~/bin/install-tibia-maps
```

## Usage

By default, `install-tibia-maps` installs the Tibia maps files with markers included:

```
$ ./install-tibia-maps
Downloading & extracting `Automap-with-markers.zip` to `~/.tibia`…
######################################################################## 100.0%
```

Use the `--no-markers` option if you want the maps without markers:

```
$ ./install-tibia-maps --no-markers
Downloading & extracting `Automap-without-markers.zip` to `~/.tibia`…
######################################################################## 100.0%
```

Example cron job to update the maps daily at midnight:

```cron
0 0 * * * /path/to/install-tibia-maps > /var/log/tibia-maps.log 2>&1
```

## Maintainer

| [![twitter/mathias](https://gravatar.com/avatar/24e08a9ea84deb17ae121074d0f17125?s=70)](https://twitter.com/mathias "Follow @mathias on Twitter") |
|---|
| [Mathias Bynens](https://mathiasbynens.be/) |
