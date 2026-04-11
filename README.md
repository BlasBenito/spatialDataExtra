# spatialDataExtra

Expands the data provided with the R package [`spatialData`](https://github.com/BlasBenito/spatialData).

## Datasets

The datasets are published as release assets here: [https://github.com/BlasBenito/spatialDataExtra/releases/latest](https://github.com/BlasBenito/spatialDataExtra/releases/latest)

### andalusia_env.tif

  - **Format**: [GeoTIFF](https://www.ogc.org/standards/geotiff)
  - **Description**: 20-layer environmental raster companion of the dataset [`spatialData::andalusia`](https://github.com/BlasBenito/spatialData/blob/main/R/andalusia.R). Covers Andalusia, Spain, at 400 m resolution in ETRS89 / UTM zone 30N (EPSG:25830). Layers include 7 Landsat TM reflectance bands (including NDVI), 2 rainfall variables, 2 solar radiation variables, 4 temperature variables, and 5 topographic variables.

To load this dataset in your R session:

```r
library(terra)
r <- terra::rast(x = "andalusia_env.tif")
```

### communities_2010.tif

  - **Format**: [GeoTIFF](https://www.ogc.org/standards/geotiff)
  - **Description**: Baseline (2010) environmental raster companion of the dataset [`spatialData::communities`](https://github.com/BlasBenito/spatialData/blob/main/R/communities.R). Covers the Sierra Nevada mountain range, SE Spain (EPSG:25830). Layers include 6 climate variables (maximum and minimum summer/winter temperature, summer and winter rainfall) and 3 topographic variables (northness, slope, topographic wetness index).

To load this dataset in your R session:

```r
library(terra)
r <- terra::rast(x = "communities_2010.tif")
```

### communities_2050.tif

  - **Format**: [GeoTIFF](https://www.ogc.org/standards/geotiff)
  - **Description**: 2050 climate scenario environmental raster companion of the dataset [`spatialData::communities`](https://github.com/BlasBenito/spatialData/blob/main/R/communities.R). Same spatial extent, resolution, and layers as `communities_2010.tif`, projected under a future climate scenario.

To load this dataset in your R session:

```r
library(terra)
r <- terra::rast(x = "communities_2050.tif")
```

### communities_2100.tif

  - **Format**: [GeoTIFF](https://www.ogc.org/standards/geotiff)
  - **Description**: 2100 climate scenario environmental raster companion of the dataset [`spatialData::communities`](https://github.com/BlasBenito/spatialData/blob/main/R/communities.R). Same spatial extent, resolution, and layers as `communities_2010.tif`, projected under a future climate scenario.

To load this dataset in your R session:

```r
library(terra)
r <- terra::rast(x = "communities_2100.tif")
```

### linaria_env.tif

  - **Format**: [GeoTIFF](https://www.ogc.org/standards/geotiff)
  - **Description**: 20-layer environmental raster companion of the dataset [`spatialData::linaria`](https://github.com/BlasBenito/spatialData/blob/main/R/linaria.R). Covers Eastern Andalusia, Spain, at 400 m resolution in ETRS89 / UTM zone 30N (EPSG:25830). Layers include 7 Landsat TM reflectance bands (including NDVI), 2 rainfall variables, 2 solar radiation variables, 4 temperature variables, and 5 topographic variables.

To load this dataset in your R session:

```r
library(terra)
r <- terra::rast(x = "linaria_env.tif")
```

### neanderthal_env.tif

  - **Format**: [GeoTIFF](https://www.ogc.org/standards/geotiff)
  - **Description**: Environmental raster companion of the dataset [`spatialData::neanderthal`](https://github.com/BlasBenito/spatialData/blob/main/R/neanderthal.R). Covers Europe and the Near East in WGS84 (EPSG:4326). Layers include 19 palaeoclimatic bioclimatic variables derived from a Last Interglacial GCM simulation (Marine Isotope Stage 5e) and 6 topographic variables (aspect, local and regional topographic diversity, elevation, slope, and topographic wetness index).

To load this dataset in your R session:

```r
library(terra)
r <- terra::rast(x = "neanderthal_env.tif")
```

### plantae.gpkg

  - **Format**: [GeoPackage](https://www.geopackage.org/)
  - **Description**: Extended version of the sf dataframe [`spatialData::plantae`](https://github.com/BlasBenito/spatialData/blob/main/R/plantae.R) with original MULTIPOLYGON ecoregion boundaries instead of point centroids. Contains 662 rows (global ecoregions) and 143 columns: 5 identifier columns, 53 response variables (plant richness, rarity-weighted richness, mean rarity, and beta diversity metrics for all plants, trees, and grasses), and 84 environmental predictors. Geometry in WGS84 (EPSG:4326).

To load this dataset in your R session:

```r
library(sf)
df <- sf::st_read(dsn = "plantae.gpkg")
```

### quercus_env.tif

  - **Format**: [GeoTIFF](https://www.ogc.org/standards/geotiff)
  - **Size**: 2.3 MB
  - **Description**: Multilayer GeoTIFF (31 layers) at ~0.167° resolution (~13-18 km depending on latitude), companion of the dataset [`spatialData::quercus`](https://github.com/BlasBenito/spatialData/blob/main/R/quercus.R). Covers Europe (12°W–34°E, 43°N–72°N) in WGS84 (EPSG:4326). Layers include 17 WorldClim bioclimatic variables (bio1–bio19, excluding bio8 and bio9), 4 NDVI statistics, 4 solar radiation statistics, 3 land cover percentages, topographic slope, topographic diversity, and human footprint index.

To load this dataset in your R session:

```r
library(terra)
r <- terra::rast(x = "quercus_env.tif")
```

### sierra_nevada_env.tif

  - **Format**: [GeoTIFF](https://www.ogc.org/standards/geotiff)
  - **Description**: Environmental raster companion of the dataset [`spatialData::interaction`](https://github.com/BlasBenito/spatialData/blob/main/R/interaction.R). Covers the Sierra Nevada mountain range, SE Spain, at 100 m resolution. Layers include 3 remote sensing variables (Landsat NDVI and two PCA scores), 5 climate variables (annual rainfall, solar radiation, mean annual temperature, maximum summer temperature, minimum winter temperature), and 2 topographic variables (topographic complexity and topographic position).

To load this dataset in your R session:

```r
library(terra)
r <- terra::rast(x = "sierra_nevada_env.tif")
```

### trees_presence.gpkg

  - **Format**: [GeoPackage](https://www.geopackage.org/)
  - **Description**: Tree species presence records associated with the dataset [`spatialData::trees`](https://github.com/BlasBenito/spatialData/blob/main/R/trees.R). Contains individual georeferenced occurrence points with columns `species` and `source`. Point geometry in WGS84 (EPSG:4326).

To load this dataset in your R session:

```r
library(sf)
df <- sf::st_read(dsn = "trees_presence.gpkg")
```

### vi.gpkg

  - **Format**: [GeoPackage](https://www.geopackage.org/)
  - **Size**: 18 MB
  - **Description**: Larger version (30,000 rows, 64 columns) of the sf dataframe [`spatialData::vi`](https://github.com/BlasBenito/spatialData/blob/main/R/vi.R). Contains global NDVI records with 5 response variable encodings (numeric, counts, binomial, categorical, factor) and 58 numeric and categorical environmental predictors covering climate, soil, topography, and biogeography. Point geometry in WGS84 (EPSG:4326).

To load this dataset in your R session:

```r
library(sf)
df <- sf::st_read(dsn = "vi.gpkg")
```
