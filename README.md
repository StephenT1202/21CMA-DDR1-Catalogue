# 21CMA-DDR1: A Point-source Catalogue of the North Celestial Pole Region

This repository hosts the **21CMA-DDR1** catalogue, which represents the first direction-dependent data release of radio point sources from the **21 CentiMeter Array (21CMA)**.

## Catalogue Overview

The 21CMA-DDR1 catalogue covers the North Celestial Pole (NCP) region (Dec > 85°), an area of approximately 78 deg². It is based on a continuous 24-hour observation obtained on **March 25, 2013**.

By implementing the `21CMAcali` pipeline, which incorporates direction-dependent calibration and wide-field imaging, we mitigate systematic effects such as grating-lobe contamination from bright sources (e.g. 3C 61.1) and ionospheric phase distortions. The final catalogue contains **1,246 radio point sources** across the 75–175 MHz frequency range.

The flux-density calibration has been re-evaluated using **LoTSS-DR3 at 144 MHz** as the external reference for post-imaging flux-density rescaling. The catalogue flux densities and their propagated formal uncertainties have been regenerated accordingly. The revised in-band spectral-index distribution has a median of **α = −0.825**.

## Data Specifications

- **Astrometry:** Source positions are systematically aligned to the **NVSS** reference frame, with an accuracy of approximately 0.1 arcmin.
- **Photometry:** Integrated flux densities are measured in five frequency products centred at **100.00, 131.25, 143.75, 156.25, and 168.75 MHz**. The flux densities have been empirically rescaled using **LoTSS-DR3** as the external reference.
- **Flux-density uncertainties:** The quoted 1σ uncertainties are the formal integrated-flux-density uncertainties returned by PyBDSF and propagated through the empirical flux-density rescaling.
- **Spectral Index:** The in-band spectral index $\alpha$ is obtained by fitting a power-law spectrum, $S \propto \nu^\alpha$, using the available 21CMA frequency measurements.

## Column Descriptions

The file `21CMA-DDR1_catalogue.csv` contains 16 data columns as defined below:

| Column | Name | Description | Units |
| :--- | :--- | :--- | :--- |
| 1 | `Source_ID` | IAU convention: `21CMA-DDR1-JHHMMSS+DDMMSS` | - |
| 2 | `RA_J2000` | Right Ascension (J2000) | h:m:s |
| 3 | `Dec_J2000` | Declination (J2000) | d:m:s |
| 4 | `Source_Type` | Morphological classification (`P` for point source) | - |
| 5 | `F100` | Integrated flux density at 100.00 MHz | Jy |
| 6 | `e_F100` | 1σ uncertainty of flux at 100.00 MHz | Jy |
| 7 | `F131` | Integrated flux density at 131.25 MHz | Jy |
| 8 | `e_F131` | 1σ uncertainty of flux at 131.25 MHz | Jy |
| 9 | `F144` | Integrated flux density at 143.75 MHz | Jy |
| 10 | `e_F144` | 1σ uncertainty of flux at 143.75 MHz | Jy |
| 11 | `F156` | Integrated flux density at 156.25 MHz | Jy |
| 12 | `e_F156` | 1σ uncertainty of flux at 156.25 MHz | Jy |
| 13 | `F169` | Integrated flux density at 168.75 MHz | Jy |
| 14 | `e_F169` | 1σ uncertainty of flux at 168.75 MHz | Jy |
| 15 | `Spectral_Index` | In-band spectral index $\alpha$ | - |
| 16 | `e_Spectral_Index` | Uncertainty of the spectral-index fit | - |
