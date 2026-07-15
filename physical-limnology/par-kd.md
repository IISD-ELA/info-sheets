# PAR and Light Attenuation (Kd) Information Sheet
**Authors:** Ken Sandilands, Paul Fafard  
**Last Updated:**  2026-07-15 by chaydata

## General

### Introduction

This information sheet describes the collection and calculation of light attenuation data collected at the IISD Experimental Lakes Area (IISD-ELA). Light data from NOLSS (Northern Ontario Lake Size Series) is also available from the IISD-ELA internal master database (collection methods may be the same). This information sheet applies to Light Transparency Profile data for Photosynthetically Active Radiation (PAR Profiles), and Light Attenuation Coefficients (Kd).

The dataset contains direct measurements of PAR, which includes wavelengths of light between 400 and 700 nm.

**Related Information sheets:** Lake Sampling & Field Observation Information Sheet

### Past data availability

1969 - 1985
* Reported attenuation coefficients for the period 1969 to 1985 are calculated using “best fit” analyses.
* “all points best fit” attenuation coefficient values, and the corresponding light profiles are not available.

1986 - 1995
* All light profiles are available and reported with “all points best fit” attenuation coefficients values.
* Currently attenuation coefficient values “using best fit” are only available for select lakes and dates.

1996 – present
* All light attenuation coefficient fields are available.

## Data Dictionary

This section has two tables:
* Definitions for the PAR dataset
* Definitions for the Light Attenuation (Kd) dataset

### Definitions for PAR dataset

| **column name (alphabetical)** | **data type** | **unit** | **definition** |
|---|---|---|---|
| account | character varying | N/A | Username of the IISD-ELA staffmember who added or most recently edited the data record. This may be generated through bulk loads or manually updated as records are edited individually. |
| avg_par_air_surface | numeric | µmol/m2/s (micromole per metre-squared per second) | Average photosynthetically active radiation (PAR) on the surface of a lake. |
| avg_par_water | numeric | µmol/m2/s (micromole per metre-squared per second) | Average photosynthetically active radiation (PAR) at a given lake depth. |
| avg_water_to_air_par_light_pct | numeric | percent | Percentage of average surface photosynthetically active radiation (PAR) at a given lake depth. |
| collection_authority | character varying | N/A | The userid of the person who is the authority or manager over the record. Often this is different from who was in the field collecting the data. This is usually similar (though not confirmed directly connected) with the current data owner specified in the ref dataset table. An example of a collection authority: for much of hydrolim data the collection authority used to be Ken Beaty but was then Ken Sandilands for more recent records, and now Paul Fafard for the most recent records. The name is typically listed as last name and first initial, e.g., SandilandsK. |
| dataset_code | character varying | N/A | A three character code made up of upper case letters and numbers unique for each dataset in ref_dataset. Should always start with a letter and may or may not end with a number. Used as a short consistent abbreviation for the dataset, whereas dataset_name is longer and may be changed and refined over time. |
| dataset_name | character varying | N/A | Name of the dataset. A dataset is a collection of data to which several individual data records (rows) belong. Dataset names are useful to distinguish groups of data across different research fields and provide some descriptive context. |
| depth_bin_m | numeric | metres | A discrete binned depth from the surface of the water, in metres. Typically this is a value derived from an original depth value using certain rounding rules. Check the info sheet for further details on how this is calculated. Binned depths are provided for convenience when wrangling data, such as to standardize depths to be able to compare between multiple profiles. |
| depth_m | numeric | metres | A depth from the surface of the water, in metres. |
| dropped_for_best_fit | boolean | N/A | True if a PAR data point has been removed from the set a of data points collected for a given lake on a given date (i.e., data point is an outlier) for the corresponding light attenuation coefficient (Kd) calculation. |
| gear_type_code | character varying | N/A | A short code that refers to a specific gear type, typically starting with two or three capital letters and ending with one number. |
| gear_type_desc | character varying | N/A | A short description of the type of gear (equipment used for sampling or surveying). Corresponds directly to the gear_type_code (one description for each code). |
| method_code | character varying | N/A | A short and unique code associated with a description of a method of sampling for data (i.e., how the physical sample was collected or measured in the field). A key to look up descriptions for codes should be included with the associated Information Sheet for the dataset in question. |
| method_description | character varying | N/A | A short description of the method used to sample the data (collect or measure the data, in a field or lab environment). For more information, see the associated Info Sheet. |
| monitoring_location_name | character varying | N/A | Name of sampled or surveyed geographic location at the IISD Experimental Lakes Area field site. The name consists of: <location> or <location sublocation> or <location sublocation station>. Location is typically the lake number (each lake is named with a number, representing the lake's geographical watershed), sublocation which typically specifies LA for "lake" (or a basin, e.g. NB - north basin, or other), and station which is usually CB ("centre buoy" - at about the deepest point of the lake). Some names do not have all three parts since a broader area is in question (e.g. for bathymetry, the entire lake, not just the centre buoy). |
| sample_date | date | date as calendar day (YYYY-MM-DD) | The day the field sampling or surveying activity was carried out to collect the data in the record. |
| sample_time | character varying | time in hours and minutes in 24 hour clock (HH:MM) | The time the field sampling or surveying activity was carried out to collect the data in the record. |
| update_date | date | date as calendar day (YYYY-MM-DD) | Date as calendar day that the record in the IISD-ELA Postgres Master Database table was uploaded to the database or most recently modified. |
| version | integer | N/A | The version number for a row of data is 1 when it is first added to a table, and increments by 1 every time the row is updated. |

### Definitions for Light Attenuation (Kd) dataset

| **column name (alphabetical)** | **data type** | **unit** | **definition** |
|---|---|---|---|
| account | character varying | N/A | Username of the IISD-ELA staffmember who added or most recently edited the data record. This may be generated through bulk loads or manually updated as records are edited individually. |
| collection_authority | character varying | N/A | The userid of the person who is the authority or manager over the record. Often this is different from who was in the field collecting the data. This is usually similar (though not confirmed directly connected) with the current data owner specified in the ref dataset table. An example of a collection authority: for much of hydrolim data the collection authority used to be Ken Beaty but was then Ken Sandilands for more recent records, and now Paul Fafard for the most recent records. The name is typically listed as last name and first initial, e.g., SandilandsK. |
| dataset_code | character varying | N/A | A three character code made up of upper case letters and numbers unique for each dataset in ref_dataset. Should always start with a letter and may or may not end with a number. Used as a short consistent abbreviation for the dataset, whereas dataset_name is longer and may be changed and refined over time. |
| dataset_name | character varying | N/A | Name of the dataset. A dataset is a collection of data to which several individual data records (rows) belong. Dataset names are useful to distinguish groups of data across different research fields and provide some descriptive context. |
| gear_type_code | character varying | N/A | A short code that refers to a specific gear type, typically starting with two or three capital letters and ending with one number. |
| gear_type_desc | character varying | N/A | A short description of the type of gear (equipment used for sampling or surveying). Corresponds directly to the gear_type_code (one description for each code). |
| kd_all_pts | numeric | m⁻¹ (metres to the power of negative 1) | Light attenuation coefficient value calculated on all original data points (where no points have been excluded). |
| kd_best_fit_pts | numeric | m⁻¹ (metres to the power of negative 1) | Light attenuation coefficient value calculated on best fit points (where outliers have been excluded if necessary). |
| method_code | character varying | N/A | A short and unique code associated with a description of a method of sampling for data (i.e., how the physical sample was collected or measured in the field). A key to look up descriptions for codes should be included with the associated Information Sheet for the dataset in question. |
| method_description | character varying | N/A | A short description of the method used to sample the data (collect or measure the data, in a field or lab environment). For more information, see the associated Info Sheet. |
| monitoring_location_name | character varying | N/A | Name of sampled or surveyed geographic location at the IISD Experimental Lakes Area field site. The name consists of: <location> or <location sublocation> or <location sublocation station>. Location is typically the lake number (each lake is named with a number, representing the lake's geographical watershed), sublocation which typically specifies LA for "lake" (or a basin, e.g. NB - north basin, or other), and station which is usually CB ("centre buoy" - at about the deepest point of the lake). Some names do not have all three parts since a broader area is in question (e.g. for bathymetry, the entire lake, not just the centre buoy). |
| num_pts_all | integer | N/A | The number of PAR data points used in calculating the light attenuation coefficient (Kd) for a given lake on a given date (where no outliers were excluded). |
| num_pts_best_fit | integer | N/A | The number of best fit PAR data points used in calculating the light attenuation coefficient (Kd) for a given lake on a given date (where outliers were excluded if necessary). |
| r2_all_pts | numeric | N/A | R2 calculated on the Log of all PAR data points for a given lake on a given date (where no data points were excluded) |
| r2_best_fit_pts | numeric | N/A | R2 calculated on the Log of best fit PAR data points for a given lake on a given date (where outliers have been excluded to bring R2 closer to 1) |
| sample_date | date | date as calendar day (YYYY-MM-DD) | The day the field sampling or surveying activity was carried out to collect the data in the record. |
| sample_time | character varying | time in hours and minutes in 24 hour clock (HH:MM) | The time the field sampling or surveying activity was carried out to collect the data in the record. |
| update_date | date | date as calendar day (YYYY-MM-DD) | Date as calendar day that the record in the IISD-ELA Postgres Master Database table was uploaded to the database or most recently modified. |
| version | integer | N/A | The version number for a row of data is 1 when it is first added to a table, and increments by 1 every time the row is updated. |

## Methods

The term “1% light depth” refers to the shallowest depth at which the underwater PAR value is ≤ 1% of the surface PAR value.

### RBR Method (2023 - present)

PAR is measured using a Licor LI-192 Underwater Quantum Sensor on an RBR Maestro<sup>3</sup> sonde, and a Licor LI-190R for surface PAR readings. A CR350 Campbell Scientific datalogger captures surface PAR readings and the streaming data from the RBR Maestro<sup>3</sup>.

When conducting a profile using the RBR method, instrumentation must be deployed on the sunny side of the boat. This includes the surface sensor, which must be situated in full sun for the duration of the profile.

The underwater PAR sensor must be positioned at the very top of the Maestro<sup>3</sup>. In this position, the PAR sensor is offset by – 0.5 m from the Maestro<sup>3</sup> depth sensor, and so the RBR must be stopped at every 0.5 m depth increment throughout the photic zone and immediately beyond the depth of 1% surface PAR, so that data for each whole m are recorded for the PAR dataset. Once through the photic zone, PAR depth is irrelevant, and the profile can continue for further collection of temperature and oxygen data.

The Campbell logger takes the average PAR values from the last 5 seconds of data for both the surface PAR sensor and underwater PAR sensor simultaneously and calculates the % of surface PAR for each depth. All data (surface PAR, underwater PAR, % of surface PAR and depth) are recorded and downloaded later from the CR350 datalogger. The use of the surface PAR sensor allows for quicker data collection than in the manual method, as the user doesn’t have to wait for constant light conditions (e.g. a cloud shadow to pass) and avoids having to redo PAR profiles under changing light conditions (see manual method below). This method also results in better readings as the user doesn’t have to pick a number midway between the fluctuation extremes as in the manual method.

<!-- Note for Chris in case I forget to ask later—the RBR par profile data has depth to mm, do we want to round the depth (after the Kd calculation) so that data could be easily comparable post 2023 to prior to 2023? -->

### Manual method (1986 to 2022, and occasionally after 2022)

The Licor LI-192 Underwater Quantum Sensor (our PAR sensor) is mounted on a frame with the sensor pointed up. The sensor is used with an LI-1400 logger, which displays the average of the last 5 seconds of data (the logger is not actually used as a data logger). To take a PAR profile, the sensor is first connected to the ‘air’ channel and held in full sun above the water surface, and a stable surface PAR value is recorded in the field book. The sensor is then connected to the ‘water’ channel, and while held at arms length on the sunny side of the boat (or the side the sun would be on if it is cloudy), is lowered into the water to 0.5 m for the first underwater reading. After a stable reading is noted in the field book for 0.5 m, stable PAR data should be recorded at each whole m depth until underwater PAR is equal to or less than 1% of surface PAR. The sensor is then brought to the surface, dried, connected to the ‘air’ channel, and a second surface PAR reading is taken. If surface PAR values differ by more than 10%, the profile is to be redone, as constant light conditions can’t be assumed for the rest of the profile.

The depth at which ≤ 1% of surface PAR occurs is considered to be the bottom of the metalimnion for integrated sampling purposes (see Lake Sampling & Field Information Sheet for a description of integrated sampling methods). Values recorded in a field book are later entered and run through an R script, where the best fit curve is determined, and light attenuation calculated.

Collection Method MIR = “Irradiance reading from digital meter”

Collection Method VIR = “Irradiance reading from analog meter”

## Data Processing

### Removal of outliers

Once the data is entered, the R<sup>2</sup> of the Log values is calculated, and data are plotted and visually inspected for outliers. If the R<sup>2</sup> is not close to 1, then outlying points are excluded manually from the calculation to achieve a higher R<sup>2</sup>.

```r
lightavg%>%
  mutate(ln_light_ratio = log(percent_light/100)) %>%
  filter(lake == 239, year == 2023, depth > 0) %>% # select L239 and 1988 as an example to look at the data
  ggplot() +
  facet_wrap(~date) +
  geom_point(aes(x = depth, y = ln_light_ratio)) +
  geom_smooth(aes(x = depth, y = ln_light_ratio), method = "lm")
```

Attenuation coefficients are calculated on both:
* The best fit (where outliers have been excluded if necessary) and R<sup>2</sup> best fit, and
* On all the data points (where no points have been excluded), and R<sup>2</sup> all points.
In each calculation, the number of points used in the calculation is reported. If points are excluded, this is indicated as “dropped for best fit” in the light transparency profiles.

Light attenuation is calculated on both the best fit curve (best R<sup>2</sup>) and on all the data (all points fit).

Once data for a field season is checked it is exported from the PAR database to the ELA data retriever. All the calculations are done in the PAR database, and results exported to the retriever.

### Light attenuation calculation

Light attenuation (Kd) is essentially the slope of natural log transformed data. Histocially Kd was calculated using VBA in an MS Access database. Now Kd is calculated using an R script. We have carefully confirmed that the script results in the same Kd values as the old formula (Ken Sandilands pers. comm., 2024-04-04). The script here is only the Kd and p-value part of a longer script by Mike Paterson, which may later be uploaded to GitHub and referenced in full.

```r

light_profiles_count <- lightavg %>%
    filter(depth > 0) %>%
    group_by(lake, date) %>%
    summarize(count = n()) %>%
    ungroup()
light_profiles_count

lightavg <- left_join(lightavg, light_profiles_count)
lightavg

light_extinction_models <- lightavg %>%
  filter(count > 2) %>%  # Mike had > 3
  mutate(ln_light_ratio = log(percent_light/100)) %>%
  group_by(lake, date, count, RBR) %>% 
  nest() %>%
  mutate(model = pmap(list(data),
                      ~ lm(ln_light_ratio ~ depth, data = ..1, na.action = na.omit)
                      )
         )
light_extinction_models


kd_results <- light_extinction_models %>% 
  mutate(slope = map_dbl(.x = model,
                             ~ round(tidy(.x)$estimate[2], digits = 3)),
         intercept = map_dbl(.x = model,
                         ~ round(tidy(.x)$estimate[1], digits = 3)),
         r_squared = map_dbl(.x = model,
                             ~ round(glance(.x)$r.squared, digits = 3)),
         p_value = map_dbl(.x = model,
                             ~ round(glance(.x)$p.value, digits = 5))
         
  )

kd_results_2 <- kd_results %>%
  mutate(Kd = slope * -1) %>%
  select(c(lake, date, Kd, intercept, r_squared, count, p_value, RBR))
```

## References

None so far
