# Sample Tables

The following examples are small real-data extracts from processed summary outputs. They document data structure and variable definitions without releasing raw climate archives, full generated panels, or complete manuscript tables.

## Bias-Adjustment Skill Summary

| source_id | edd_bin | mean_dskill_mae | median_dskill_mae | sd_dskill_mae | n |
|---|---|---:|---:|---:|---:|
| EC-Earth3 | edd_8 | 21.9173 | 0.0000 | 129.1599 | 30492 |
| GFDL-ESM4 | edd_8 | 55.6764 | 1.9752 | 168.1381 | 30492 |
| MPI-ESM1-2-HR | edd_8 | 30.1916 | 0.0000 | 135.1824 | 30492 |

## Crop-Threshold Skill Differences

| source_id | crop | n | edd_0 | edd_8 | edd_28 |
|---|---|---:|---:|---:|---:|
| EC-Earth3 | maize | 4356 | 71.0924 | 35.7926 | -0.9493 |
| EC-Earth3 | rice | 4356 | 25.8671 | 14.6720 | -0.4266 |
| EC-Earth3 | wheat | 4356 | 48.1777 | 18.4389 | -0.5630 |

## Raw Model MAE Summary

| source_id | edd_bin | mean_mae | median_mae |
|---|---|---:|---:|
| CNRM-CM6-1 | edd_8 | 109.8940 | 60.8257 |
| CNRM-CM6-1-HR | edd_8 | 86.5529 | 58.4922 |
| EC-Earth3 | edd_8 | 82.9410 | 57.1648 |

## Compact Public-Paper Summary

| source_id | edd_0 | edd_4 | edd_8 | edd_12 | edd_28 | edd_30 | edd_32 |
|---|---:|---:|---:|---:|---:|---:|---:|
| EC-Earth3 | 53.2003 | 38.3423 | 21.9173 | 3.6891 | -0.7513 | 0.1361 | 0.3330 |
| GFDL-ESM4 | 111.0130 | 84.9879 | 55.6764 | 24.2307 | -2.0362 | -1.1108 | -0.5454 |
| MPI-ESM1-2-HR | 63.4653 | 47.8259 | 30.1916 | 11.0865 | -1.0116 | -0.2110 | 0.0932 |

## Interpretation

- `edd_bin`: extreme-degree-day threshold bin.
- `mean_dskill_mae`: average reduction in mean absolute error from raw to bias-adjusted climate product; positive values indicate improvement.
- `source_id`: climate model identifier.
- `n`: number of model-region-crop-irrigation-period-threshold records in the summarized group.
- `mean_mae`: mean absolute error of raw CMIP6 exposure relative to ERA5.
- Positive public-summary values indicate mean MAE improvement after bias adjustment; negative values indicate degradation.
