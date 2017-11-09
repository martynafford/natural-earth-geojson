# Natural Earth data in GeoJSON

[Natural Earth](http://www.naturalearthdata.com) "is a public domain map dataset available at 1:10m, 1:50m and 1:110 million scales."
The vector data comes as [ESRI shapefiles](http://www.esri.com/library/whitepapers/pdfs/shapefile.pdf).
This repository provides the same data but converted to [GeoJSON](http://geojson.org), along with a compressed version.

<img src="logo.png">

The conversion is performed using [ogr2ogr](http://www.gdal.org/ogr2ogr.html), part of the [Geospatial Data Abstraction Library](http://www.gdal.org) (GDAL).
GDAL provides [links to binaries](https://trac.osgeo.org/gdal/wiki/DownloadingGdalBinaries).
Debian provides the package [gdal-bin](https://packages.debian.org/gdal-bin).

## Data Themes

An overview of the files, taken from the [features page](http://www.naturalearthdata.com/features).

### Cultural

| Section | Description | 1:10m | 1:50m | 1:110m |
| --- | --- | --- | --- | --- |
| Countries | Matched boundary lines and polygons with names attributes for countries and sovereign states. Includes dependencies (French Polynesia), map units (U.S. Pacific Island Territories) and sub-national map subunits (Corsica versus mainland Metropolitan France). | Yes | Yes | Yes |
| Disputed areas and breakaway regions | From Kashmir to the Elemi Triangle, Northern Cyprus to Western Sahara. | Yes | Yes | |
| First order admin | Provinces, departments, states, etc. Internal boundaries and polygons for all but a few tiny island nations. Includes names attributes and some statistical groupings of the same for smaller countries. | Yes | Yes | |
| Populated places | Point symbols with name attributes. Includes capitals, major cities and towns, plus significant smaller towns in sparsely inhabited regions. We favor regional significance over population census in determining rankings. | Yes | Yes | Yes |
| Urban polygons | Derived from 2002-2003 MODIS satellite data. | Yes | Yes | |
| Parks and protected areas | U.S. National Park Service units. | Yes | | |
| Pacific nation groupings | Boxes for keeping these far-flung islands tidy. | Yes | Yes | Yes |
| Water boundary indicators | Partial selection of key 200-mile nautical limits, plus some disputed, treaty, and median lines. | Yes | | |

### Physical

| Section | Description | 1:10m | 1:50m | 1:110m |
| --- | --- | --- | --- | --- |
| Coastline | Ocean coastline, including major islands. Coastline is matched to land and water polygons. | Yes | Yes | Yes |
| Land | Land polygons including major islands | Yes | Yes | Yes |
| Ocean | Ocean polygon split into contiguous pieces. | Yes | Yes | Yes |
| Minor Islands | Additional small ocean islands ranked to two levels of relative importance. | Yes | | |
| Reefs | Major coral reefs from WDB2. | Yes | | |
| Physical region features | Polygon and point labels of major physical features. | Yes | Yes | Yes |
| Rivers and Lake Centerlines | Ranked by relative importance. Includes name and line width attributes. Don't want minor lakes? Turn on their centerlines to avoid unseemly data gaps. | Yes | Yes | Yes |
| Lakes | Ranked by relative importance, coordinating with river ranking. Includes name attributes. | Yes | Yes | Yes |
| Glaciated areas | Polygons derived from DCW, except for Antarctica derived from MOA. Includes name attributes for major polar glaciers. | Yes | Yes | Yes |
| Antarctic ice shelves | Derived from 2003-2004 MOA. Reflects recent ice shelf collapses. | Yes | Yes | |
| Bathymetry | Nested polygons at 0, -200, -1,000, -2,000, -3,000, -4,000, -5,000, -6,000, -7,000, -8,000, -9,000,and -10,000 meters. Created from SRTM Plus. | Yes | | |
| Geographic lines | Polar circles, tropical circles, equator, and International Date Line. | Yes | Yes | Yes |
| Graticules | 1-, 5-, 10-, 15-, 20-, and 30-degree increments. Includes WGS84 bounding box. | Yes | Yes | Yes |

## Version

Data used is [version 4.0.0](http://www.naturalearthdata.com/updates/mail.cgi?flavor=archive;list=updates;id=20171103122417) (released 2017-11-03), the latest as of 2017-11-03.

## Disclaimer

The Natural Earth [disclaimer regarding disputed areas](http://www.naturalearthdata.com/downloads/10m-cultural-vectors/10m-admin-0-countries/):

> Natural Earth Vector draws boundaries of countries according to de facto status.
> We show who actually controls the situation on the ground.
> Please feel free to mashup our disputed area themes to match your particular political outlook.

