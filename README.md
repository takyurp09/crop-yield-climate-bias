# Crop Yield Climate Bias Adjustment

This repository contains a public portfolio version of a climate-data pipeline for evaluating how raw CMIP6, bias-adjusted CMIP6, and ERA5 reanalysis differ when estimating crop-relevant extreme heat exposure.

The workflow focuses on extreme degree days (EDD) during crop growing seasons, combining large climate archives with crop calendars, harvested-area weights, and regional agricultural units.

## Why This Repository Matters

This project demonstrates research computing skills that are useful for agricultural economics, climate-risk modeling, and Earth-system data analysis:

- handling large ERA5 and CMIP6 climate archives;
- accessing cloud-hosted climate data through ESGF, Pangeo, and Microsoft Planetary Computer workflows;
- calculating crop-calendar-specific extreme heat metrics;
- harmonizing gridded climate data with administrative agricultural units;
- comparing raw and bias-adjusted model performance against ERA5;
- building reproducible R and Python pipelines for maps, diagnostics, and tables.

## Repository Structure

```text
00_config.R                         Shared paths and analysis settings
01_load_harmonize.R                 Load and harmonize model/reanalysis panels
02_metrics.R                        Bias-adjustment skill and error metrics
03_maps.R                           Spatial diagnostics
04_plots.R                          Performance and distributional plots
05_generate_paper_tables.R          Summary table generation
06_generate_conference_figures.R    Selected figure generation
run_all.R                           Master workflow
python_scripts/
  era5_*.py                         ERA5 extreme-degree-day processing
  esgf_*.py                         Raw CMIP6 access and EDD construction
  pc_*.py                           Bias-adjusted CMIP6 access and EDD construction
docs/
  DATA_SOURCES.md                   Data provenance and access notes
  REPRODUCIBILITY.md                Environment and run-order notes
  PUBLIC_RELEASE_CHECKLIST.md       Safe-public-release checklist
figures/selected/
  Selected public-facing diagnostics and workflow visual
```

## Selected Visuals

![Spatial bias-adjustment skill](figures/selected/spatial_bias_adjustment_skill.png)

![Workflow overview](figures/selected/workflow_overview.svg)

## Data Availability

Raw climate and agricultural data are not committed because the workflow depends on large external archives and provider-specific access routes. See `docs/DATA_SOURCES.md`.

## Public-Release Scope

This repository excludes raw climate data, generated panels, manuscript files, submission materials, and local machine metadata. It is intended to show coding style, data-engineering choices, workflow organization, and reproducibility practice.
