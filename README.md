# Tibia maps installer for Linux [![Build status](https://travis-ci.org/tibiamaps/tibia-maps-installer-linux.svg)](https://travis-ci.org/tibiamaps/tibia-maps-installer-linux)

`install-tibia-maps` is a Bash script that downloads the latest version of the `minimap` data provided by [the tibia-map-data project](https://github.com/tibiamaps/tibia-map-data) and extracts it to the `~/.local/share/CipSoft\ GmbH/Tibia/packages/Tibia` folder.

## Installation

Store this script locally and run it again every now and then to update your maps to the latest version.

```sh
curl https://raw.githubusercontent.com/tibiamaps/tibia-maps-installer-linux/main/install-tibia-maps > ~/bin/install-tibia-maps; chmod +x ~/bin/install-tibia-maps
```

## Usage

By default, `install-tibia-maps` installs the Tibia maps files with markers included:

```
$ ./install-tibia-maps
Downloading & extracting `minimap-with-markers.zip`…
######################################################################## 100.0%
```

Use the `--no-markers` option if you want the maps without markers:

```
$ ./install-tibia-maps --no-markers
Downloading & extracting `minimap-without-markers.zip`…
######################################################################## 100.0%
```

Use the `--grid` option if you want the maps with the overlay grid and the markers:

```
$ ./install-tibia-maps --grid
Downloading & extracting `minimap-with-grid-overlay-and-markers.zip`…
######################################################################## 100.0%
```

Use the `--grid-no-markers` option if you want the maps with the overlay grid but without markers:

```
$ ./install-tibia-maps --grid-no-markers
Downloading & extracting `minimap-with-grid-overlay-without-markers`…
######################################################################## 100.0%
```

Use the `--grid-poi-markers` option if you want the maps with the overlay grid and [points of interest markers](https://tibiamaps.io/blog/speedrun-poi):

```
$ ./install-tibia-maps --grid-poi-markers
Downloading & extracting `minimap-with-grid-overlay-and-poi-markers`…
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
