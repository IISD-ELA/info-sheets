# Meteorology – Air Pressure – Information Sheet
Authors: Chris Hay

## Contents
- [General Information](#general-information)
  * [Background of the datasets](#background-of-the-datasets)
  * [Considerations and applications](#considerations-and-applications)
- [Methods](#methods)
  * [Site Location](#site-location)
  * [Date and Time](#date-and-time)
  * [Instrumentation](#instrumentation)
  * [Limitations](#limitations)
  * [Gear type codes](#gear-type-codes)
- [Data Dictionary](#data-dictionary)
- [References](#references)

## General Information

### Background of the datasets

Air pressure is measured as absolute atmospheric pressure in millibars, at the IISD Experimental Lakes Area meteorological site. The meteorological site has received instrumentation and support by Environment Canada (ECCC) since it was established. Publicly available data from Environment Canada instrumentation at the IISD-ELA meteorological station (called Rawson Lake (AUT)) is also available, online at [https://tinyurl.com/ELAmetsite](https://tinyurl.com/ELAmetsite). Some records in our dataset originate from the ECCC dataset, as both instruments are maintained at the IISD-ELA metsite, and work well to fill gaps when one or the other is not working. ECCC data are also used for quality control to cross-compare sensors. We acknowledge these contributions to increase the value and usability of the air pressure dataset, and refer to ECCC's data licence for more information: [https://climate.weather.gc.ca/prods_servs/attachment1_e.html](https://climate.weather.gc.ca/prods_servs/attachment1_e.html).

### Considerations and applications

*This section still needs to be filled out, ideally drawing from expert knowledge of our hydrolim team and research scientists.*

<!-- EXAMPLE FROM air-temperature.md, for the kind of thing that should go here:

Data that is collected, processed and analysed is utilized by a variety of research projects, scientists and graduate students from both within and outside of IISD-ELA. Many of the datasets are long term (now 50+ years) and provide understanding of natural variability in our ecosystems and will be valuable in future for studies such as climate change. They have proven invaluable in the planning of new experiments.

The majority of data in the daily maximum/minimum air temperature dataset was collected using manual read thermometers. From 2011-11-02 to 2017-11-20, data from manual thermometers and digital air temperature probes were being collected, and so these dates will have data from both methods. Since 20 November 2017, manual thermometers were discontinued and air temperature data is sourced from digital temperature probes. -->

## Methods

### Site Location

The IISD-ELA meteorological station ("METSITE" in the data tables) is land based and is located 370 m west of Rawson Lake (L239), 400 m northwest of the field station, and 43 m above the lake surface. Altitude above sea level is 433m.

UTM Coordinates:
* 15 U 0447128 5501551 (NAD83)  
* 15 U 0447138 5501331 (NAD27)  

DMS Coordinates:
* 49°39′51″ N
* 93°43′58″ W

### Date and Time

Unlike the IISD-ELA air temperature and precipitation datasets which use climatological day (starting at 8AM CST for the IISD-ELA metsite), the air pressure dataset uses regular calendar days, in CST time year-round.

### Instrumentation

IISD-ELA atmospheric pressure is collected with our sensor... (additional details may be added in future). Our dataset also includes some records from Environment Canada's atmospheric pressure sensor, when our sensor is down or recorded incorrect values. Both sensors are near each other at the IISD-ELA meteorological station.

### Limitations

*This section still needs to be filled out, ideally drawing from expert knowledge of our hydrolim team and research scientists.*

<!-- Example of the kind of content that could go in this section, from the air-temperature.md info sheet:

Mercury freezes at -39 <sup>o</sup>C. At this temperature, mercury within the thermometer will not move and will no longer give completely reliable data. Records exist with the ELA database below these temperatures; these records should be used with caution.

The T107C temperature probe has measurement limitation to between 50 <sup>o</sup>C and -35 <sup>o</sup>C. The Vaisala HMP 45C probe has a measurement limitation of -39.2 <sup>o</sup>C. The HygroVUE 10 sensor has a measurement limitation of -40 <sup>o</sup>C. Temperatures below these should be used with caution.

Data from the manually read/reset alcohol/mercury thermometers, and so has potential error due poor reading or incomplete reset. All data from the thermometers is rounded to the nearest 0.5 <sup>o</sup>C when read.

Data from digital probes is high quality, high resolution data, though potential error exists due to sensor drift between re-calibrations. -->


### Gear type codes

* ATM1: IISD-ELA ATMOSPHERIC PRESSURE SENSOR
* ATM2: ENVIRONMENT CANADA ATMOSPHERIC PRESSURE SENSOR


## Data Dictionary

In the ELA database, units of measure are as follows:

- Time is always Central Standard Time (CST) (GMT-6)
- Date is calendar day (not climatological day)
- Air pressure is measured as absolute atmospheric pressure in millibars (mbar)

**Column name (alphabetical)** | **data type** | **unit** | **definition** 
---|---|---|---
 abs_atmpress_mbar | numeric | millibars | Absolute atmospheric pressure value, which is defined as the force of the weight of the atmosphere's air, per unit area, relative to a perfect vacuum, for a specific time and location on earth. 
 account | character varying | N/A | Username of the IISD-ELA staffmember who added or most recently edited the data record. This may be generated through bulk loads or manually updated as records are edited individually. 
 dataset_code | character varying | N/A | A three character code made up of upper case letters and numbers unique for each IISD-ELA dataset. Should always start with a letter and may or may not end with a number. Used as a short consistent abbreviation for the dataset, whereas dataset_name is longer and may be changed and refined over time. 
 dataset_name | character varying | N/A | Name of the dataset. A dataset is a collection of data to which several individual data records (rows) belong. Dataset names are useful to distinguish groups of data across different research fields and provide some descriptive context. Directly associated with dataset_code (each code has a different name). 
 date | date | YYYY-MM-DD | The calendar or climatological day (YYYY-MM-DD) for the associated record, indicating when the observation, measurement, sample collection, or other recording method happened. All air temperature and precipitation datasets from IISD-ELA are based on the climatological day (at IISD-ELA, 8AM CST is used as the start of the climatological day) using the Meteorological Service of Canada’s definition of climatological day (see the info sheets for more information). Other datasets use regular calendar days. 
 gear_type_code | character varying | N/A | A short code that refers to a specific gear type, typically starting with two or three capital letters and ending with one number. 
 gear_type_desc | character varying | N/A | A short description of the type of gear (equipment used for sampling or surveying). Corresponds directly to the gear_type_code (one description for each code). 
 monitoring_location_name | character varying | N/A | Name of sampled or surveyed geographic location at the IISD Experimental Lakes Area field site. 
 time | time without time zone | HH:MM:SS | The time the field sampling or surveying activity was carried out to collect the data in the record. 
 update_date | date | N/A | Date as calendar day that the record in the IISD-ELA Postgres Master Database table was uploaded to the database or most recently modified. 
 version | numeric | N/A | The version number for a row of data is 1 when it is first added to a table, and increments by 1 every time the row is updated. 


## References

Environment Canada data: https://tinyurl.com/ELAmetsite  

Licence Agreement for Use of Environment and Climate Change Canada Data: https://climate.weather.gc.ca/prods_servs/attachment1_e.html
