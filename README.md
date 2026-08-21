# MaaNTE MapSource

Static Leaflet map assets for [MaaNTE-Map](https://github.com/Maa-NTE/MaaNTE-Map).

The `tiles/{z}/{x}/{y}.jpg` pyramid contains the expanded map in 512px JPEG
tiles, zoom levels `-6` through `0`, compressed at quality 88. The map
application references the raw GitHub URL directly, so only small web tiles
are stored in this repository. Source/composite images remain local and are
not committed here.

## Layout

- `tiles/`: compressed Leaflet tiles consumed by the web map.
