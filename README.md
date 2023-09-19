# Mapping Server based on OSM Stack

!WiP

This whole repository is just a starting point of loose coupled experiments to get a deep dive into OSM Development!

This setup reflects a mapping server based on the OSM stack.

https://switch2osm.org/serving-tiles/manually-building-a-tile-server-ubuntu-22-04-lts/

## Unordered information

### Postgres

Postgres Commands
```
sudo -u postgres -i
psql
\c gis2
\dn
\dt+
```

### Carto

Stylesheet for the rendering of tiles

https://wiki.openstreetmap.org/wiki/OpenStreetMap_Carto

### Slippy Map

Explaining Slippy map

https://wiki.openstreetmap.org/wiki/Slippy_map#OpenStreetMap_.22Standard.22_tile_server

### Edit Data

See the additional layers, currently not being rendered (all the piles in harbour wellingdorf)

https://www.openstreetmap.org/search?query=schleswig%20holstein#map=18/54.32938/10.17173&layers=D

![Data Map](images/data_map.png)

Watch the video to see, how piles are being created.

![create piles](images/how_to_create_a_mooring_pile.mov)

### Vagrant Machine

Install the dependencies (homebrew!)

```
brew install vagrant
brew install --cask virtualbox
```

start up the vagrant machine

```
vagrant up
```

The vagrant machine makes use of the hostmanager plugin, which adds domain entries toe the hosts /etc/hosts file.

Open the browser on

http://osm.lokal/#8/54.448/10.040 
