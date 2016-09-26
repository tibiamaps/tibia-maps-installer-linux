#!/usr/bin/env bash

mkdir -p ~/.tibia;
if [ "${1}" = '--no-markers' ]; then
	echo 'Downloading & extracting `Automap-without-markers.zip` to `~/.tibia`…';
	url='https://tibiamaps.io/downloads/automap-without-markers';
else
	echo 'Downloading & extracting `Automap-with-markers.zip` to `~/.tibia`…';
	url='https://tibiamaps.io/downloads/automap-with-markers';
fi;
zip_file_name="$(mktemp)";
curl --progress-bar --location "${url}" > "${zip_file_name}";
unzip -o -d ~/.tibia "${zip_file_name}";
rm "${zip_file_name}";
