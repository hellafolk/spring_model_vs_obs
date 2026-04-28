# Data Sources

---

## Observational Data (obtain manually)

### ATom DC-8 Aircraft
- **Description:** NASA Atmospheric Tomography Mission merged 1 Hz data files (MER-1HZ format)
- **Format:** ICARTT (.ict)
- **Period:** 2016–2018 (ATom-1 through ATom-4)
- **Source:** NASA ESPO Archive — https://espo.nasa.gov/atom
- **Place in:** `data/observations/atom/`

### TransFuture 5 (TF5) Shipboard Picarro
- **Description:** Continuous atmospheric CO₂ from a Picarro analyzer aboard a Japanese cargo vessel
- **Format:** NetCDF (.nc)
- **Period:** 2016–2018
- **Source:** NOAA GML
- **Place in:** `data/observations/ship/`
- **Filename:** `co2_tf5_shipboard-insitu_20_allvalid.nc`

### POC Shipboard Flask
- **Description:** Discrete atmospheric CO₂ flask samples from a NOAA GML research vessel
- **Format:** NetCDF (.nc)
- **Period:** 2016–2018
- **Source:** NOAA GML — https://gml.noaa.gov/dv/data/
- **Place in:** `data/observations/ship/`
- **Filename:** `co2_poc_shipboard-flask_1_representative.nc`

---

## Model Reference Products (obtain manually)

### NOAA Global MBL
- **Description:** Globally averaged CO₂ on a sine-latitude grid, 41 bands
- **Format:** Plain text
- **Source:** https://gml.noaa.gov/ccgg/mbl/
- **Place in:** `data/mbl/mbl_global/`
- **Filename:** `surface.mbl.co2`

### NOAA Pacific MBL
- **Description:** Pacific-optimized CO₂ on a sine-latitude grid, 41 bands
- **Format:** Plain text
- **Source:** https://gml.noaa.gov/ccgg/mbl/
- **Place in:** `data/mbl/mbl_pacific/`
- **Filename:** `surface.mbl.co2`

### NOAA GHG MBL Reference
- **Description:** Global MBL reference with uncertainty estimates, 13 sine-latitude bands
- **Format:** Plain text
- **Source:** https://gml.noaa.gov/ccgg/mbl/
- **Place in:** `data/mbl/`
- **Filename:** `co2_GHGreference.*.txt`

---

## Remote Sensing and Reanalysis (downloaded automatically by notebook)

### OISST Sea Surface Temperature
- **Description:** NOAA Optimum Interpolation SST, monthly, 0.25° resolution
- **Source:** NOAA ERDDAP — https://coastwatch.pfeg.noaa.gov/erddap
- **Downloaded to:** `data/remote_sensing/sst_oisst_tropics_monthly_2016_2018.nc`

### MODIS-Aqua Chlorophyll-a
- **Description:** Monthly chlorophyll-a concentration, 4 km resolution
- **Source:** NASA CoastWatch ERDDAP — https://coastwatch.pfeg.noaa.gov/erddap
- **Downloaded to:** `data/remote_sensing/chl_modis_tropics_YYYY.nc` (one file per year)

### ERA5 Wind Speed and Surface Pressure
- **Description:** Monthly mean 10m wind components and mean sea level pressure, 0.25° resolution
- **Source:** Copernicus Climate Data Store — https://cds.climate.copernicus.eu
- **Requires:** Free CDS account and API key in `~/.cdsapirc`
- **Downloaded to:** `data/remote_sensing/era5_slp_wind_tropics_2016_2018.nc`

### CarbonTracker CT2022
- **Description:** Monthly planetary boundary layer CO₂ (pbl_co2), 3°×2° resolution
- **Source:** NOAA GML — https://gml.noaa.gov/ccgg/carbontracker/
- **Downloaded to:** `data/remote_sensing/carbontracker/CT2022.molefrac_glb3x2_YYYY-MM.nc`
