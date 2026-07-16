# Data Sources

This project combines gridded climate archives with crop calendars, harvested area, and administrative boundaries.

## Climate Data

| Source | Role | Access route |
|---|---|---|
| ERA5 reanalysis | Benchmark climate record for EDD comparison | Copernicus Climate Data Store |
| Raw CMIP6 | Unadjusted GCM climate simulations | ESGF / Pangeo cloud catalogs |
| Bias-adjusted CMIP6 / CIL-GDPCIR | Bias-adjusted climate projections | Microsoft Planetary Computer |

## Agricultural and Spatial Data

| Source | Role |
|---|---|
| SAGE crop calendars | Defines planting, between-season, and harvest windows |
| GAEZ harvested area | Crop-specific harvested-area weights |
| GADM administrative boundaries | Aggregation from gridded climate data to regional units |

## Public Repository Policy

Large raw climate files, downloaded NetCDF/Zarr stores, shapefiles, and generated Parquet panels are excluded from Git. Users should obtain data directly from source providers and place them in a local `data/` directory.

Recommended local layout:

```text
data/
  raw/
  external/
  processed/
```
