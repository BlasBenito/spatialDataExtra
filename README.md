# spatialDataExtra

Expands the data provided with the R package [`spatialData`](https://github.com/BlasBenito/spatialData). The data is not in this repo, instead it is provided as release assets. Please check the [Releases](https://github.com/BlasBenito/spatialDataExtra/releases) page.                                                                  

## Datasets

### vi.gpkg

  - **Format**: [GeoPackage](https://www.geopackage.org/)
  - **Size**: 18 MB
  - **Description**: Larger version (30,000 rows, 64 columns) of the sf dataframe [`spatialData::vi`](https://github.com/BlasBenito/spatialData/blob/main/R/vi.R). Contains global NDVI records with 5 response variable encodings (numeric, counts, binomial, categorical, factor) and 58 numeric and categorical environmental predictors covering climate, soil, topography, and biogeography. Point geometry in WGS84 (EPSG:4326).

To load this dataset in your R session:

```r
library(spatialData)
df <- vi_extra()
```

### plantae.gpkg

  - **Format**: [GeoPackage](https://www.geopackage.org/)
  - **Size**: 18.5 MB
  - **Description**: POLYGONS version of the POINT sf dataframe [`spatialData::plantae`](https://github.com/BlasBenito/spatialData/blob/main/R/plantae.R). Plant richness and betadiversity data and predictors for the world's ecoregions. Point geometry in WGS84 (EPSG:4326).

To load this dataset in your R session:

```r
library(spatialData)
df <- plantae_extra()
```


### quercus_env.tif

  - **Format**: [GeoTIFF](https://www.ogc.org/standards/geotiff)
  - **Size**: 2.3 MB
  - **Description**: Multilayer GeoTIFF (31 layers) at ~0.167° resolution (~13-18 km depending on latitude), companion of the dataset [`spatialData::quercus`](https://github.com/BlasBenito/spatialData/blob/main/R/quercus.R). Covers Europe (12°W–34°E, 43°N–72°N) in WGS84 (EPSG:4326). Layers include 17 WorldClim bioclimatic variables (bio1–bio19, excluding bio8 and bio9), 4 NDVI statistics, 4 solar radiation statistics, 3 land cover percentages, topographic slope, topographic diversity, and human footprint index.
  
To load this dataset in your R session:

```r
library(spatialData)
library(terra)
r <- quercus_extra()
```

### neanderthal_env.tif

  - **Format**: [GeoTIFF](https://www.ogc.org/standards/geotiff)
  - **Size**: 6.24 MB
  - **Description**: Multilayer GeoTIFF (31 layers) at ~0.167° resolution (~13-18 km depending on latitude), companion of the dataset [`spatialData::neanderthal`](https://github.com/BlasBenito/spatialData/blob/main/R/neanderthal.R). Covers Europe and North Africa in WGS84 (EPSG:4326). Layers include 17 WorldClim palaeoclimatic variables (bio1–bio19, excluding bio8 and bio9) and several topographic variables.
  
To load this dataset in your R session:

```r
library(spatialData)
library(terra)
r <- neanderthal_extra()
```
