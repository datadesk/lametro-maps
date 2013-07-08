# Los Angeles Metro Maps

Geospatial data from the L.A. Metro's public transportation system

## Sources

Existing lines and stops published by L.A. Metro
http://developer.metro.net/introduction/gis-data/download-gis-data/

Planned lines and stop estimated by me, Ben Welsh, based on flat map's published by L.A. Metro
http://www.metro.net/projects/connector/

## Process

1. Navigate to http://developer.metro.net/introduction/gis-data/download-gis-data/
2. Locate a dataset in the "ESRI Shapefile" format
3. Download the zip file
4. Use ogr2ogr to convert to `.geojson` with the `crs:84` SRS

## Bulk processing

1. Follow the steps above to download one or more zipped shapefiles
2. Run [this shell script](https://gist.github.com/benbalter/5858851)

## Requirements to convert

To convert shapefiles to geojson and reproject, you'll need [ogr2ogr](http://www.gdal.org/ogr2ogr.html). On OS X, the easiest way to do this is with [Homebrew](http://mxcl.github.io/homebrew/), by running the command `brew install gdal`.

## Contributing

1. Fork the project
2. Add a `.geojson` file
3. Submit a pull request

## Much respect due

This repository was inspired by Derek Willis' [nyc-maps](https://github.com/dwillis/nyc-maps/)

