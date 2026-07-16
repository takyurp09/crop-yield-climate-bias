# Method Overview

This project evaluates whether bias-adjusted climate products improve crop-relevant extreme heat exposure measurement relative to raw CMIP6 outputs, using ERA5 as the reanalysis benchmark.

## Core Objects

| Object | Unit | Description |
|---|---|---|
| Crop-calendar EDD | region x crop x irrigation x period x year | Extreme degree days computed inside crop-relevant growing windows |
| Paired climate spine | model x region x crop x irrigation x period x threshold x year | Harmonized ERA5, raw CMIP6, and bias-adjusted CMIP6 comparison panel |
| Bias-adjustment skill | model x region x crop x irrigation x period x threshold | Difference in error metrics between raw and bias-adjusted products |

## Conceptual Steps

1. Access ERA5, raw CMIP6, and bias-adjusted CMIP6 climate products.
2. Compute extreme degree days at multiple temperature thresholds.
3. Align gridded climate exposure with crop calendars and harvested-area weights.
4. Aggregate exposure to agricultural administrative units.
5. Compare raw and bias-adjusted products against ERA5 using MAE, RMSE, quantile, tail, KS, and correlation diagnostics.
6. Summarize performance by model, crop, irrigation status, period, threshold, and spatial unit.

## Why This Is Useful

Crop-yield and food-security analysis depends on how climate exposure is measured. This workflow demonstrates how large climate archives can be converted into crop-specific exposure measures while checking whether bias adjustment actually improves the agricultural signal.

## Public Release Note

This repository is a portfolio-safe release. It documents the research-computing workflow without publishing raw climate archives, generated full panels, manuscript files, or complete result tables.
