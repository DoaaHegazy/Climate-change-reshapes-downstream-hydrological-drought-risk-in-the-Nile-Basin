
# Climate Change Reshapes Downstream Hydrological Drought Risk in the Nile Basin

This repository provides the reproducible computational workflow used to investigate drought propagation and future hydrological drought risk in the Nile River Basin, with a focus on downstream impacts at Dongola.

## Study Overview

Downstream regions of the Nile Basin, particularly Sudan and Egypt, rely heavily on upstream precipitation. This study examines how upstream climate variability propagates through the hydrological system and affects downstream hydrological drought conditions.

The analysis integrates climate projections, hydrological modeling, and extreme value theory to quantify future drought risk under climate change scenarios.

## Methodology

The workflow combines climate data processing, hydrological modeling, and statistical analysis:

- Bias-corrected CMIP6 climate projections (SSP2-4.5 and SSP5-8.5)
- Model selection based on SPI-12 drought frequency
- SWAT+ hydrological modeling for streamflow simulation
- Hydrological drought characterization using SRI-12
- Extreme value analysis of annual minimum SRI-12

## Workflow Overview

The analysis is implemented through the following structured pipeline:

1. **SPI-12 computation and model selection**  
   Compute SPI-12 from bias-corrected CMIP6 precipitation and select representative climate models (dry, median, wet futures).

2. **SWAT+ input preparation**  
   Convert selected climate model outputs into SWAT/SWAT+ weather input format.

3. **Hydrological simulation**  
   Simulate historical and future streamflow using a calibrated SWAT+ model.

4. **Hydrological drought analysis (SRI-12)**  
   Compute SRI-12 from streamflow to quantify hydrological drought conditions.

5. **Annual maximum series extraction (AMS)**  
   Extract annual maximum drought severity time series.

6. **Extreme value and return period analysis**  
   Estimate drought return periods using extreme value theory.

## Notebooks

| Notebook | Description |
|---|---|
| 01_SPI12_climate_models.ipynb | SPI-12 computation and climate model selection |
| 02_SWAT_inputs_Format.ipynb | Conversion of climate data to SWAT/SWAT+ format |
| 03_SRI12_historical_future.ipynb | SRI-12 computation from streamflow |
| 04_AMS_drought.ipynb | Annual maximum drought severity extraction |
| 05_Extreme_analysis_return_period.ipynb | Extreme value and return period analysis |

## Data Availability

Due to data size constraints, large datasets (CMIP6 NetCDF files, SWAT+ outputs) are not included in this repository.

The complete reproducibility package is archived on Zenodo:

**DOI:** (to be added)

## Software

All analyses were conducted in Python using Jupyter notebooks with the following libraries:

- NumPy, pandas
- SciPy (extreme value analysis)
- xarray (NetCDF processing)
- geopandas (spatial data)
- matplotlib (visualization)

## Author

Doaa Hegazy  
PhD Student, Department of Geological and Environmental Sciences  
Western Michigan University
