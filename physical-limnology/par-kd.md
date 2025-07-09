# PAR Light Attenuation: Physical Limnology Information Sheet

Authors: Ken Sandilands, Paul Fafard  

## IISD-ELA Database Fields for PAR

* Location ID, Sublocation, Station ID  
* Date and Time (CST)  
* Attenuation Coefficient – best fit  
* R<sup>2</sup> best fit  
* \# of Points – best fit  
* Atten. Coeff. – all points  
* R<sup>2</sup> all points fit  
* \# of points – all points fit  
* Depth (m)  
* % of Surface Light  
* Light Value (PAR) (µmol/m<sup>2</sup>/s)  
* Dropped for best fit?  
* Collection Method  
* Dataset ID =  

## General

This information sheet describes the collection and calculation of light attenuation data collected at the Experimental Lakes Area. Light data from NOLSS (Northern Ontario Lake Size Series) is also in the ELA data retriever (Collection methods may be the same?). This information sheet applies to Light Transparency Profile data, and Light Attenuation Coefficients. These are data for PAR at lake surface and within the water column.

The dataset contains direct measurements of Photosynthetically Active Radiation (PAR), which includes wavelengths of light between 400 and 700 nm.

<u>Related Information sheets</u>

Lake Sampling & Field Observation Information Sheet

## Collection Method

<u>Instrumentation 2023 - present</u>

PAR is measured using a Licor LI-192 Underwater Quantum Sensor on an RBR Maestro, and a Licor LI-190R for surface PAR readings with a CR350 Campbell Scientific datalogger which captures the streaming data from the RBR Maestro.

<u>Instrumentation (pre 2023)</u>

Photosynthetically Active Radiation (PAR) is measured with an underwater Licor PAR sensor (model LI 192 Underwater Quantum Sensor), and a LI-1400 logger for reading out the values only (not used as a datalogger).

Collection Method MIR = “Irradiance reading from digital meter”

Collection Method VIR = “Irradiance reading from analog meter”

<u>Methods</u>

The term “1% light depth” refers to the shallowest depth at which the underwater PAR value is ≤ 1% of the surface PAR value.

<u>RBR Method</u>

PAR is measured using a Licor LI-192 Underwater Quantum Sensor on an RBR Maestro<sup>3</sup> sonde, and a Licor LI-190R for surface PAR readings. A CR350 datalogger captures surface PAR readings and the streaming data from the RBR Maestro<sup>3</sup>.

When conducting a profile using the RBR method, instrumentation must be deployed on the sunny side of the boat. This includes the surface sensor, which must be situated in full sun for the duration of the profile.

The underwater PAR sensor must be positioned at the very top of the Maestro<sup>3</sup>. In this position, the PAR sensor is offset by – 0.5 m from the Maestro<sup>3</sup> depth sensor, and so the RBR must be stopped at every 0.5 m depth increment throughout the photic zone and immediately beyond the depth of 1% surface PAR, so that data for each whole m are recorded for the PAR dataset. Once through the photic zone, PAR depth is irrelevant, and the profile can continue for further collection of temperature and oxygen data.

The Campbell logger takes the average PAR values from the last 5 seconds of data for both the surface PAR sensor and underwater PAR sensor simultaneously and calculates the % of surface PAR for each depth. All data (surface PAR, underwater PAR, % of surface PAR and depth) are recorded and downloaded later from the CR350 datalogger. The use of the surface PAR sensor allows for quicker data collection than in the manual method, as the user doesn’t have to wait for constant light conditions (e.g. a cloud shadow to pass) and avoids having to redo PAR profiles under changing light conditions (see manual method below). This method also results in better readings as the user doesn’t have to pick a number midway between the fluctuation extremes as in the manual method.

Note for Chris in case I forget to ask later—the RBR par profile data has depth to mm, do we want to round the depth (after the Kd calculation) so that data could be easily comparable post 2023 to prior to 2023?

<u>Manual method (1986 to 2022, and occasionally after 2022)</u>

The Licor LI-192 underwater quantum sensor is mounted on a frame with the sensor is pointed up. The sensor is used with an LI-1400, which displays the average of the last 5 seconds of data. To take a PAR profile, the sensor is first connected to the ‘air’ channel and held in full sun above the water surface, and a stable surface PAR value is recorded in the field book. The sensor is then connected to the ‘water’ channel, and while held at arms length on the sunny side of the boat (or the side the sun would be on if it is cloudy), is lowered into the water to 0.5 m for the first underwater reading. After a stable reading is noted in the field book for 0.5 m, stable PAR data should be recorded at each whole m depth until underwater PAR is equal to or less than 1% of surface PAR. The sensor is then brought to the surface, dried, connected to the ‘air’ channel, and a second surface PAR reading is taken. If surface PAR values differ by more than 10%, the profile is to be redone, as constant light conditions can’t be assumed for the rest of the profile.

The depth at which ≤ 1% of surface PAR occurs is considered to be the bottom of the metalimnion for integrated sampling purposes (see Lake Sampling & Field Information Sheet for a description of integrated sampling methods). Values recorded in a field book are later entered and run through an R script, where the best fit curve is determined, and light attenuation calculated.

<u>Data Processing</u>

Removal of outliers

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

*<u>Light attenuation calculation</u>*

Light attenuation (Kd) is essentially the slope of natural log transformed data. Histocially Kd was calculated using VBA in an MS Access database. Now Kd is now calculated using an R script. We have carefully confirmed that the script results in the same Kd values as the old formula (Ken Sandilands pers. comm., 2024-04-04). The script here is only the Kd and p-value part of a longer script by Mike Paterson, which may later be uploaded to GitHub and referenced in full.

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

<u>Past data availability</u>

1969 - 1985
* Reported attenuation coefficients for the period 1969 to 1985 are calculated using “best fit” analyses.
* “all points best fit” attenuation coefficient values, and the corresponding light profiles are not available.

1986 - 1995
* All light profiles are available and reported with “all points best fit” attenuation coefficients values.
* Currently attenuation coefficient values “using best fit” are only available for select lakes and dates.

1996 – present
* All light attenuation coefficient fields are available.

<u>Data Sets</u>

G05 - VERTICAL ATTENUATION COEFFICIENTS - PRIOR TO 1986 – All data are using the “best fit” analyses, the
