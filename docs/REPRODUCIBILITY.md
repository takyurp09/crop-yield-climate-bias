# Reproducibility

This repository is a public, lightweight release of a larger climate-data workflow. It tracks source code, documentation, selected visuals, and a portable environment specification.

## Environment

```bash
conda env create -f environment.yml
conda activate crop-yield-climate-bias
```

The Python scripts require access to large climate archives. Some sources may need provider accounts, local credentials, or cloud access configuration.

## Suggested Run Order

1. Build ERA5 EDD panels with `python_scripts/era5_*.py`.
2. Build raw CMIP6 EDD panels with `python_scripts/esgf_*.py`.
3. Build bias-adjusted CMIP6 EDD panels with `python_scripts/pc_*.py`.
4. Configure local paths in `00_config.R`.
5. Run `run_all.R` or execute the R scripts in sequence:
   - `01_load_harmonize.R`
   - `02_metrics.R`
   - `03_maps.R`
   - `04_plots.R`
   - `05_generate_paper_tables.R`
   - `06_generate_conference_figures.R`

## Notes

The public version is not a turnkey reproduction package because raw climate archives are too large for Git and require external access. The repository documents the workflow and code structure needed to reproduce the analysis once source data are configured locally.
