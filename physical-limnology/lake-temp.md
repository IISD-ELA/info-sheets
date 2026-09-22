# Lake Temperature at the Surface and via Strings - Information Sheet
**Authors:** Ken Beaty; Ken Sandilands; Paul Fafard; Chris Hay  
**Last Updated:**  2026-09-22 by chaydata


## Contents
- [General Information](#general-information)
    - [Datasets Overview](#datasets-overview)
    - [Surface Temperature Background](#surface-temperature-background)
    - [Temperature Strings Background](#temperature-strings-background)
- [Methods](#methods)
    - [Surface Temperature Instrumentation](#surface-temperature-instrumentation)
        - [VPT - manual thermometer readings](#vpt---manual-thermometer-readings)
        - [LS1 - floating analog temp loggers](#ls1---floating-analog-temp-loggers)
        - [LS2 - floating digital temp loggers](#ls2---floating-digital-temp-loggers)
        - [LS3 - digital water level and temperature loggers](#ls3---digital-water-level-and-temperature-loggers)
    - [Temperature String Instrumentation](#temperature-string-instrumentation)


- [Data Dictionary](#data-dictionary)
    - [Tables and Lists of Columns](#list-of-columns)
        - [Ice Phenology - Table info and columns](#ice-phenology---table-info-and-columns)
        - [Ice Watch - Table info and columns](#ice-watch---table-info-and-columns)
    - [Column Definitions](#column-definitions)
        - [Ice Phenology - Column Definitions](#ice-phenology---column-definitions)
        - [Ice Watch - Column Definitions](#ice-watch---column-definitions)
    - [Parameter Definitions](#parameter-definitions)

- [References](#references)

## General Information

### Datasets Overview

**This info sheet covers ***two*** datasets:**
* Surface Temperature
* Littoral Temperature Strings

**Related datasets in other info sheets:**
* Stream Temperature: See [Hydrology - Stream Temperature](../hydrology/stream-temp.md)
  * Although similar methods are used for stream surface temperature as lake surface temperature, streams are categorized as hydrological data, so a separate info sheet is used
* Profiles: See [Physical Limnology - Profiles (Multiparameter Sondes and Historical Methods)](/profiles.md)
  * These "profiles" are indeed very similar to the temperature strings dataset described in this info sheet, especially when considering historical profile data that started with only temperature measurements.
  * Differences:
    * Collection method: The "profiles" dataset was always manual sondes lowered into the water, whereas temperature strings stay in the water all season and automatically collect data
    * Temporal resolution: Since "profiles" are manually collected, they are done less frequently (usually every two weeks), whereas since the temperature strings work automatically, they collect data several times a day (e.g. hourly)
    * Multiparameter vs. temperature-only: The "profiles" started with only temperature but later added oxygen, and more recently include multiple parameters (pH, conductivity, chlorophyll-a), whereas the temperature strings only collect temperature data.

### Surface Temperature Background

**The IISD-ELA dataset for surface temperature consists of data collected using three different methods, with the longest dataset for Lake 239.**

Lake surface temperature is one of several components measured at IISD Experimental Lakes Area, with the record beginning on May 02, 1969 for Lake 239. Surface water temperature is used in hydrometeorological studies for evaporation calculations. In addition to this data set, daily mean values of Lake 239 surface temperatures were recorded on a data logger on an instrument tower installed by Environment Canada from 1969 – 1971. These data can be found in Beaty (1981) Appendix 8, Tables 81-83.

Lake surface temperature data is utilized by a variety of research projects, scientists and graduate students from both within and outside of IISD-ELA. Long term datasets provide understanding of natural variability in our ecosystems and are valuable for studies such as climate change. They have also proven invaluable in the planning of new experiments.

A table of lakes and data collection date ranges for each lake is included below. Additional temperature string data also exist for some lakes, collected by the ELA Fish Crew.

| **Lake** | **Date range** |
|----|----|
| L114 | 2000-2026 (hourly) |
| L224 | 2000-2026 (hourly) |
| L226 | 1997-1998 (hourly) |
| L227 | 2008-2013, 2022-2026 (hourly) |
| L239 | 1969-1997 (daily), 1998-2026 (hourly) |
| L239 streams (NWIF, NEIF, EIF) | 2018-2026 (hourly) |
| L260 | 1999-2004, 2017-2026 (hourly) |
| L302 S | 2008 (hourly) |
| L303 | 2009-2011, 2023-2026 (hourly) |
| L304 | 2009-2011, 2023-2026 (hourly) |
| L373 | 2000 – 2026 (hourly) |
| L378 | 2020 – 2026 (hourly) |
| L442 | 2000-2019, 2021-2026 (hourly) |
| L626 | 2008-2013, 2022-2026 (hourly) |
| L632 | 1992-1995 (daily) |
| L658 | 2001-2009 (hourly) |
| L979 | 1992-1993 (daily), 1994 (half-hourly), 1995 (daily), 1997-1998, 2001, 2006 (hourly) |

### Temperature Strings Background

Temperature strings (or "pelagic/limnetic temperature loggers") are essentially strings with sensors attached at certain intervals, reaching into the depths of a lake. On our lakes, they are stationed in the *open area* of the lake (pelagic/limnetic; as opposed to the littoral area closer to shore).  

Here is a summary of historical* data availability:
| **Lake** | **Date range** |
|----|----|
| 222 | 2013-2019 (hourly) |
| 223 | 2013-2019 (hourly) |
| 224 | 2013-2019 (hourly) |
| 239 | 2013-2019 (hourly) |
| 240 | 2016-2019 (hourly) |
| 260 | 2013-2019 (hourly) |
| 373 | 2013-2019 (hourly) |
| 626 | 2013-2019 (hourly) |

\* *Note: More recent records after 2019 are also available, but have not yet been integrated into our master database.*  

## Methods

### Surface Temperature Instrumentation

Over the years lake surface temperature has been collected by one of 3 basic methods. Records in the data set are coded with the following codes: VPT (manual thermometer readings), LS1 (floating analog temp logger), and LS2 (floating digital temp logger). As of 2023, stream temperature data are logged digitally using a combined water level and temperature data logger (LS3).

#### VPT - manual thermometer readings

This method was used from 1969 to 1979. The longer style Hg thermometers were used to take manual readings to the nearest 0.5°C. These measurements were taken manually (Qualifier code A, not sure if measurements were taken at the dock or centre buoy).

#### LS1 - floating analog temp loggers

This method was used from 1979 to 1988. Peabody Ryan model J thermographs were installed on a floating raft. Daily means were calculated from an average of 4 data points per day from the paper chart record. Accuracy of ±2% or 0.6°C.

#### LS2 - floating digital temp loggers

From 1989 to 1997 Richard Branker XL-800 temperature loggers were used to provide daily mean temperatures. These loggers have an accuracy of 0.1°C. Daily mean temperatures were assigned a timestamp of 12:00.

From 1998 to 2007 HOBO Onset Optic Stow Away temp loggers were used. These loggers have an accuracy of 0.1°C. Hourly mean temperatures provide a timestamp for each record. Means are from measurements taken from the hour previous to the recorded time (e.g. 08:00 data record is from measurements between 07:00 and 08:00).

From 2008 to 2021 HOBO Water Temp Pro v2 loggers were used. These loggers have an accuracy of 0.2 °C. In addition to the HOBO Water Temp Pro v2 loggers, HOBO MX2201 temperature loggers were deployed in 2019, and have an accuracy of 0.5 ºC. In 2021, TinyTag Aquatic 2 TG-4100 temperature loggers were trialed. The Aquatic 2 loggers replaced HOBO loggers starting in the 2022 field season. TinyTag Aquatic 2 loggers have an accuracy of 0.5 ºC.

These floating digital temp loggers are deployed during the ice-free period. Loggers are attached to the centre buoy and downloaded periodically throughout the season. Depending on the method of attachment, and style of logger, these loggers are situated ~10-15 cm below the lake surface.

#### LS3 - digital water level and temperature loggers

This method was used from 2023 onwards, for stream temperature datasets. Solinst Levelogger 5 (model 3001) water level and temperature loggers are deployed on streambeds housed in perforated white PVS tubes that shield the logger from direct light but allows unimpeded flow of water past sensor. Accuracy of 0.05°C.

### Temperature String Instrumentation

Stream temperature and temperature string data have been collected using HOBO Pendant UA-001 or UA-002 data loggers. These loggers have an accuracy of 0.53 ºC.

Temperature loggers in streams have typically been anchored in place using a small weight, and were deployed in within easy reach for downloading. No shielding was used to protect loggers from direct sunlight.

Solinst Levelogger 5 (model 3001) water level and temperature loggers have been in use since 2023 for all streams. The Solinst Levelogger 5 (model 3001) have an accuracy of 0.05 ºC.

## References

Beaty K.G. 1981. Hydrometeorological Data for the Experimental Lakes Area, Northwestern Ontario, 1969 through 1978 Part I. Can. Data Rep. Fish. Aquat. Sci. 285: vi + 1-97.
