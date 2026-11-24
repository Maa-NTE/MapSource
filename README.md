# MaaNTE MapSource

Static Leaflet map assets for [MaaNTE-Map](https://github.com/Maa-NTE/MaaNTE-Map).

The `tiles/{z}/{x}/{y}.jpg` pyramid contains the expanded map in 512px JPEG
tiles, zoom levels `-6` through `0`, compressed at quality 88. The map
application references the raw GitHub URL directly, so only small web tiles
are stored in this repository. Source/composite images remain local and are
not committed here.

## Layout

- `tiles/`: compressed Leaflet tiles consumed by the web map.

## Native source

Refreshed on 2026-11-25 from the exported game textures under
`/Game/UI/UI/minimap/13-bigworldmap-1/`. FModel MCP confirmed the active
`XL_map_bigworld_test` row in `/Game/DataTable/MiniMap/DT_LevelMiniMap` uses
this texture set.

The source contains 2,601 opaque 512px PNGs, `map_bigworld_10001` through
`map_bigworld_12601`, arranged in row-major order as a 51 by 51 grid.
Its full extent is 26,112 by 26,112 pixels. The generated pyramid contains
3,516 tiles across zoom levels -6 through 0, using bicubic downsampling,
JPEG quality 88, and RGB `(14, 28, 29)` padding outside the image extent.
The extent and orientation match the existing MaaNTE-Map coordinate frame.
