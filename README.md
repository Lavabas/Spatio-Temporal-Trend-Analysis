# Spatio-Temporal Trend Analysis using Mann-Kendall Test in Python API (Xee)

## Overview
This project applies the Mann-Kendall trend test to analyze long-term temperature patterns from 1980 to 2025 across the central region of Sri Lanka using ECMWF ERA5 monthly temperature data. By leveraging the Xee API, which acts as a bridge between Google Earth Engine (GEE) and xarray in Python, the workflow enables advanced statistical testing on time-series geospatial datasets directly in Python.

The Mann-Kendall test is a non-parametric method used widely in climate science to detect monotonic trends in a time series. Here, it is applied pixel-wise to identify spatially distributed increasing, decreasing, or neutral temperature trends over 40+ years.

## Data Source
| Dataset            | Provider                                                | Temporal Range | 
| ------------------ | ------------------------------------------------------- | -------------- |
| ECMWF ERA5 Monthly | Copernicus / Google Earth Engine (`ECMWF/ERA5/MONTHLY`) | 1980–2025      | 


## Output
<img width="781" height="204" alt="image" src="https://github.com/user-attachments/assets/16f2fe8e-7239-47a8-9bbf-4edf702a4001" />

- Left: Trend classification (1 = increasing, -1 = decreasing, 0 = no trend)
- Center: MK Score (S-statistic, scaled)
- Right: MK p-values (Significant regions shown as p < 0.05)

## Notes
- The Xee API allows direct xarray-style access to GEE imagery with CRS and scale options.
- No preprocessing was needed for temperature data as ERA5 is cloud-free (unlike optical imagery).
- Output visualizations were generated with matplotlib using plt.tight_layout() to maintain clarity.




