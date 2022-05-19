## Pune Watershed Overlap Map

Developed by Nikhil VJ for CEE India in 2019
Contact: nikhil.js (at) gmail (dot) com


Watershed raster images shared by CEE were geoferenced on QGIS using [Freehand raster georeferencer plugin](https://plugins.qgis.org/plugins/FreehandRasterGeoreferencer/) , then broken up into XYZ map tiles (using [QTiles plugin](https://plugins.qgis.org/plugins/qtiles/) in QGIS itself).

HTML file contains javascript to load map and change the tile source for a layer depending on dropdown selection.

The generated map tiles, being of v.high number, are hosted at: https://server.nikhilvj.co.in/watershed_overlap_map/tiles/ instead of on github.

This work is published under MIT Open License for open sharing

## Running on local system

If you just want to see the changing overlay tiles and don't care about the boundary layers, then you can just open the .html in your web browser; should run directly.

To load the boundary layers, a http server like setup is needed as the .geojson shapes are loaded dynamically and browsers don't allow this with html's opened from local folder.

Pls run python's simple http server command in the same folder, or please get an equivalent local web server software (you can find many on the web)
```
python -m http.server
```
Note: if your system has both python 2 and 3, then you may need to type "python3" instead of "python"

Then this folder will be deployed on http://localhost:8000

----


