# Meteorology – Relative Humidity – Information Sheet
Authors: Ken Beaty, Ken Sandilands, Paul Fafard

## Contents
- [General Information](#general-information)
  * [Background of the datasets](#background-of-the-datasets)
  * [Considerations and applications](#considerations-and-applications)
- [Methods](#methods)
  * [Site Location](#site-location)
  * [Past methods](#past-methods)
  * [Instrumentation](#instrumentation)
- [Data Dictionary](#data-dictionary)
- [References](#references)

<!-- **IISD-ELA Database Fields for Relative Humidity:**

Location ID, Sublocation, Station ID  
Measurement Date (YYYY-MM-DD)  
Hour (HH:MM CST, hour ending)  
Relative Humidity (%)  
Collection Method (LM1, LM2, LM3, LM4, LM5)  
Data Set ID = M11  
Environment Canada public data for IISD Experimental Lakes Area found below:  
Rawson Lake (AUT): <https://tinyurl.com/ELAmetsite> -->

## General information

Relative humidity is the ratio of the amount of moisture in a given space to the amount the space could contain if saturated, expressed as a percentage. These data were collected, along with air temperature, to calculate the actual vapour pressure tern in empirical evaporation equations that only required mean daily or mean monthly values. Measuring devices, methods and data resolution have improved over time as better equipment and computing technology became available. This progression has evolved from manual sling psychrometers, wet/dry bulb hygrometers, chart recorders that employ a hygroscopic hair element to modern digital data loggers and sensors having greater sensitivity and resolution. Instrumentation was located in a Stevenson screen shelter.

The IISD-ELA database contains logged hourly relative humidity data starting 1 January 2007. Data up to the end of 1987 was published in Beaty 1981, Beaty 1984 and Beaty and Lyng 1989, and is not currently in the IISD-ELA database.

## Methods

### Site Location

The IISD-ELA meteorological station ("METSITE" in the data tables) is land based and is located 370 m west of Rawson Lake (L239), 400 m northwest of the field station, and 43 m above the lake surface. Altitude above sea level is 433m.

UTM Coordinates:
* 15 U 0447128 5501551 (NAD83)  
* 15 U 0447138 5501331 (NAD27)  

DMS Coordinates:
* 49°39′51″ N
* 93°43′58″ W

### Past methods

Collection of relative humidity data at the ELA met site began in May 1970. In that first year, values reported were the average of readings taken from a wet/dry bulb hygrometer twice daily at 08:00 and 19:00 CST. In 1971, values from May 11 to June 6 were based on the average of readings taken at 07:00 and 12:00 CST. Mean daily values from June 7 to the end of the season in 1992 were determined by hand scaling weekly charts from a Casella London recording thermohygrograph. All original charts are on file at IISD-ELA storage. Routine checks were made using either a sling psychrometers or a ventilated hygrometer to verify the reliability of the recorder.

### Instrumentation

In January 1993, a Campbell Scientific 21X data logger was installed by Environment Canada at the met site which included a sensor for relative humidity. The raw data files provide average hourly values. The loggers were upgraded to a CS-23X on August 5, 2009 and to a CR3000 on November 2, 2011. These loggers, sensors, and data belong to and have been maintained by Environment Canada.

On July 31, 2007, a Campbell Scientific CR1000 data logger owned by IISD-ELA was installed at the met site which collected hourly relative humidity data, along with other parameters.

The following section is meant to document data contained in the IISD-ELA database. See "past methods" section above for a description of data prior to 1 January 2007.

**These codes are used in the IISD-ELA database in the Collection Methods field.**

> LM1 – Digital relative humidity data up to 5 August 2009. Logged hourly data was captured on the CS-21X logger using a Vaisala HMP 35A.
>
> LM2 - 6 August 2009 to 2 Nov 2011. Logged hourly data captured on the CS-23X logger using a Vaisala HMP 45C temperature and relative humidity probe.
>
> LM3 - 2 November 2011 to current. Logged hourly data captured on the CR3000 datalogger (ECCC) with a Vaisala HMP 45C temperature and relative humidity probe. Data may be used to fill gaps in LM4 and LM5 data.
>
> LM4 - 31 July 2007 to 16 August 2022. Logged hourly data captured on IISD-ELA CR1000 datalogger with an HMP 45C temperature and relative humidity probe (6-wire).
>
> LM5 – 16 August 2020 to current. Logged data captured on IISD-ELA CR1000 datalogger with a HygroVUE 10 temperature and humidity sensor. This data is the primary source of RH data since deployment. This data may also be used to fill gaps in the LM3 data.

## Data Dictionary

 **Column name (alphabetical)** | **data type** | **unit** | **definition** 
---|---|---|---
 account | character varying | N/A | Username of the IISD-ELA staffmember who added or most recently edited the data record. This may be generated through bulk loads or manually updated as records are edited individually. 
 dataset_code | character varying | N/A | A three character code made up of upper case letters and numbers unique for each IISD-ELA dataset. Should always start with a letter and may or may not end with a number. Used as a short consistent abbreviation for the dataset, whereas dataset_name is longer and may be changed and refined over time. 
 dataset_name | character varying | N/A | Name of the dataset. A dataset is a collection of data to which several individual data records (rows) belong. Dataset names are useful to distinguish groups of data across different research fields and provide some descriptive context. 
 date | date | N/A | The calendar or climatological day (YYYY-MM-DD) for the associated record, indicating when the observation, measurement, sample collection, or other recording method happened. All air temperature and precipitation datasets from IISD-ELA are based on the climatological day (at IISD-ELA, 8AM CST is used as the start of the climatological day) using the Meteorological Service of Canada’s definition of climatological day (see the info sheets for more information). Other datasets use regular calendar days. 
 hour | numeric | N/A | Hour of the day as an integer number, from 0 to 23. Hours are "hour ending", for example, hour 2 is the end of the second hour. 
 method_sample_code | character varying | N/A | A short and unique code associated with a description of a method of sampling for data (i.e., how the physical sample was collected or measured in the field). 
 method_sample_desc | character varying | N/A | A short description of the method used to sample the data (collect or measure the data, in a field or lab environment). For more information, see the associated Info Sheet. 
 monitoring_location_name | character varying | N/A | Name of sampled or surveyed geographic location at the IISD Experimental Lakes Area field site. 
 relative_humidity_percent | numeric | percent | Relative humidity is the ratio of the amount of moisture in a given space to the amount the space could contain if saturated, expressed as a percentage. See the info sheet for more information. 
 update_date | date | N/A | Date as calendar day that the record in the IISD-ELA Postgres Master Database table was uploaded to the database or most recently modified. 
 version | numeric | N/A | The version number for a row of data is 1 when it is first added to a table, and increments by 1 every time the row is updated. 



## References

Beaty, K.G. 1981. Hydrometeorological data for the Experimental Lakes Area, northwestern Ontario, 1969 through 1978 (in three parts). Can. Data Rep. Fish. Aquat. Sci. 285

Beaty, K. G. 1984. Hydrometeorological data for the Experimental Lakes Area, northwestern Ontario, 1979 – 1981. Can. Data Rep. Fish. Aquat. Sci. 480

Beaty, K. G. and M.E. Lyng. 1989. Hydrometeorological data for the Experimental Lakes Area, northwestern Ontario, 1982-1987. Can. Data Rep. Fish. Aquat. Sci. 759
