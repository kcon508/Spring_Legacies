# Spring_Legacies
Data and analysis associated with Ecosphere submission
- initial submit 14 April 2025

# Analysis 
All analysis is combined in "Ecosphere Spring Legacies MS Analysis.Rmd"

within that file: 
1. VWC (0-20 cm)
2. GCC
3. Efflux
4. ANPP
5. PRS N
6. Sentek (0-50 cm VWC)
7. Precipitation 

(See annotations in code for more)

# Data files
### SGS_SLs_20cmVWC_all.csv
Associated with (1) VWC 0-20cm

- Date: date of measurements
- Plot: plot # 1-50 but only 40 used
- NewTrt: plot treatment assignment (ambient, ambient w/ deluge, or dry w/ deluge)
- Comb.TRT: duplicate of NewTrt w/ pre-deluge addition dates combining ambient treatments
- VWC: VWC measurement (VWC %)

### SGS_SLs_GCC_all.csv
Associated with (2) GCC

- Date: see above
- Plot: see above
- NewTrt: see above
- GCC: GCC ratio output after R image analysis
- Drop: y/n drop image due to low quality or other issues (flags in image, etc.)

### SGS_SLs_Respiration_all.csv
Associated with (3) Efflux

- Date: see above
- Plot: see above
- NewTrt: see above
- Soil_Temp: ºC soil temperature at 10cm depth
- VWC: 20cm VWC measure (matches SGS_SLs_20cmVWC_all.csv if taken same date)
- Efflux: soil CO2 efflux output (µmol CO2 per m2 per s)
- Drop_resp: y/n drop observation due to sensor issues or other notes from field
- Drop_temp: y/n drop observation due to sensor issues or other notes from field

### SGS_SLs_ANPP_all.csv
Associated with (4) ANPP

- Plot: see above
- Clip_Type: clip = July harvest, reclip = mid to late regrowth harvest, TOTAL = sum of July clip + regrowth reclip, clip2 = September (end of season) harvest
- TRT: see "NewTrt" above
- Comb.TRT: see "Comb.TRT" above
- ANPP: Total ANPP from harvest (g/m2)
- Total.Grasses: Gramminoid only biomass (g/m2)

### SGS_SLs_PRS_NO3droppedlow.csv
Associated with (5) PRS Nitrate-N
- Sample_ID: ID associated with analysis by Western Ag
- Anion: # of anion probes included in analysis (typically 3)
- Cation: # of cation probes included in analysis (typically 3)
- TRT: see "NewTrt" above
- Plot: see above
- Nutrient: NO3.N = Nitrate nitrogen
- rate: probe uptake (µg per 10cm2 membrane surface per 60 day burial)
(see https://www.westernag.ca/innovations/technology/basics)

### SGS_SLs_2021_Interpolated_Sentek_VWC.csv
Associated with (5) Sentek
- doy: Day of year (1-366) of observation (defined w/ origin in associated code to proper date - starting 1/1/2021)
- VWC: VWC % measurement
- depth: 10-100cm depth of measurement
- Plot: see above
- Trt: see "NewTrt" above

### SGS_Precip_Combined.csv
Associated with (6) Precipitation

- new.Date: dates of observation
- NOAA_mm: precipitation nearest NOAA station
- Notes: notes on gap filling or missing values
- n.times: # of combined observations if daily data is sum of multiple times
- USDA_mm: daily USDA data provided by CPER
- yr: starting 1990 - year of date
- mon: starting 1990 - month of date
- usda_20to21: duplicate of USDA_mm split into single yr and 2021 missing filled with NOAA_mm
- NOAA_mm2: duplicate of NOAA_mm w/o NA's



