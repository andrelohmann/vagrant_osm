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

### Mapnik

https://wiki.openstreetmap.org/wiki/DE:Mapnik

### Carto

Stylesheet for the rendering of tiles

https://wiki.openstreetmap.org/wiki/OpenStreetMap_Carto

https://wiki.openstreetmap.org/wiki/CartoCSS

https://wiki.openstreetmap.org/wiki/OpenStreetMap_Carto/Symbols

https://github.com/gravitystorm/openstreetmap-carto/blob/master/USECASES.md

### Seamarks

We need to use the seamark type "mooring" with category "pile" (Dalben).

https://wiki.openstreetmap.org/wiki/Seamarks/Seamark_Objects

https://github.com/OpenNauticalChart/renderer <- maybe we can steal from here

https://wiki.openstreetmap.org/wiki/Tag:man_made%3Ddolphin

https://wiki.openstreetmap.org/wiki/Tag:seamark:type%3Dpile

https://wiki.openstreetmap.org/wiki/Tag:seamark:type%3Dmooring


### Slippy Map

Explaining Slippy map

https://wiki.openstreetmap.org/wiki/Slippy_map#OpenStreetMap_.22Standard.22_tile_server

### Edit Data

See the additional layers, currently not being rendered (all the piles in harbour wellingdorf)

https://www.openstreetmap.org/search?query=schleswig%20holstein#map=18/54.32938/10.17173&layers=D

https://www.openstreetmap.org/edit#map=21/54.32957/10.17308

![Data Map](images/data_map.png)

Watch the video to see, how piles are being created.

[create piles](images/create_mooring_pile.mov)

<video width="320" height="240" controls>
  <source src="https://github.com/andrelohmann/vagrant_osm/raw/main/images/create_mooring_pile.mov" type="video/mp4">
</video>

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

### Browse the tile server

Open the browser on

http://osm.lokal/#8/54.448/10.040
