# Precipitation: Hydrometeorology Information Sheet

Authors: Paul Fafard, Ken Sandilands  
Last update: April 15<sup>th</sup>, 2024 (PF)

# IISD-ELA Database Fields for Precipitation:

Daily (Climatological Day)  
Location ID, Sublocation, Station ID  
Measure Date (YYYY-MM-DD)  
Rain (mm), Snow (mm), Trace (\<0.1 mm)  
Data Set ID = M01

Environment Canada public data for IISD Experimental Lakes Area found below:

Rawson Lake (AUT): <https://tinyurl.com/ELAmetsite>

# General

**The IISD-ELA dataset for daily precipitation consists of the twice-daily manual readings of the standard rain gauge (parts of spring and fall, summer) and once-daily manual readings of the nipher (parts of spring and fall, winter).**

Daily precipitation is one of several components measured at the IISD Experimental Lakes Area meteorological site, with the record beginning on June 27, 1969. The meteorological site has received instrumentation and support by Environment Canada since it was established. Publicly available data from Environment Canada instrumentation at the IISD-ELA meteorological station (called Rawson Lake (AUT)) is at the URL above.

Data that is collected, processed and analysed is utilized by a variety of research projects, scientists and graduate students from both within and outside of IISD-ELA. Many of the data sets are long term (now 40+ years) and provide understanding of natural variability in our ecosystems and will be valuable in future for studies such as climate change. They have proven invaluable in the planning of new experiments.

# Site Location

The site is land based and is located 370 m west of Rawson Lake (L239), 400 m northwest of the field station, and 43 m above the lake surface.

UTM Coordinates  
15 U 0447128 5501551 (NAD83)  
15 U 0447138 5501331 (NAD27)

# Collection Methods

<u>Climatological day</u>

All precipitation and air temperature data in the IISD-ELA database is based on the **climatological day** (for ELA, 8AM CST is used as the start of the climatological day) using the Meteorological Service of Canada’s definition of climatological day:

> *Observations taken based on a calendar day cannot capture the minimums and maximums that are truly reflective of the peaks and lows over a 24-hour period. Normally, the coldest period in any given day is just before sunrise and the warmest period in a day is shortly after the sun reaches its zenith in the afternoon. A climatological day was therefore developed to ensure that the maximum and minimum temperatures could be captured. The climatological day tends to start and end at the same hour of two consecutive days. For example, the climatological day begins at the 0601 UTC observations on Day 1 and ends at the 0600 UTC observation on Day 2.*
>
> *For sites that report two observations over a 24-hour period, MSC uses the following procedure to determine:*

- *Maximum temperature: For "today" is calculated from the maximum temperature reported for "today's" afternoon (PM) observation compared to the maximum temperature reported for "tomorrow's" morning (AM) observation;*

- *Minimum temperature: For "today" is calculated from the minimum temperature reported for "today's" morning (AM) observation and for "today's" afternoon (PM) observation;*

- *Rainfall, snowfall and precipitation totals: For "today" are calculated from "today's" afternoon (PM) observation with "tomorrow's" morning (AM) observation; and*

- *Snow on the ground: For "today" is based on "today's" morning (AM) observation.*

Daily rain gauge checks occur twice per day; once at 08:00 CST and once at ~20:00 CST. The precipitation level within the rain gauge is read and the rain gauge is emptied at these times.

Time periods for precipitation in the IISD-ELA database are as follows:

“Today’s” precipitation is the total of the amount in the rain gauge at the 20:00 CST check plus the amount in the rain gauge at the 08:00 CST check the following day.

E.g.
| August 25 |     | August 26 |     | August 27 |     |
| --- | --- | --- | --- | --- | --- |
| 08:00 CST | 20:00 CST | 08:00 CST | 20:00 CST | 08:00 CST | 20:00 CST |
| Trace | 0.0 mm | 0.0 mm | 1.2 mm | 1.0 mm | Trace |

The data in this table show that August 26 had a daily precipitation of 2.2 mm. The August 26 20:00 CST rain gauge value is the total precipitation during the 12-hour period of 08:00 – 20:00 on August 26. The August 27 08:00 CST rain gauge value is the total precipitation during the 12-hour period of 20:00 CST August 26 – 08:00 CST August 27. The daily total is the combined value from these two 12-hour periods.

During winter months, the standard rain gauge (SRG) is discontinued and the nipher gauge is deployed, as it does a better job of catching snow and other freezing precipitation. The nipher cylinder is left out for 24 hours and swapped with a clean nipher cylinder only once per day at the 08:00 CST station check. Any frozen precipitation within the nipher is melted and measured in a calibrated glass graduate. This graduate is calibrated to convert the melted precipitation from the nipher to a water equivalent value to match a standard rain gauge. In this way, snow and other frozen precipitation can be measured in mm, as rainfall is measured in a standard rain gauge. Values recorded from the nipher are daily totals for the previous day’s precipitation.

<u>Instrumentation</u>

The standard instrument for measuring precipitation is the white plastic type B metric rain gauge (SRG) for temperatures above 0 <sup>o</sup>C, and the nipher gauge for temperatures below 0 <sup>o</sup>C. Currently, the meteorological site is equipped with type B metric rain gauge/nipher gauge as well as a tipping bucket rain gauge (TBRG) connected to a data logger. The SRG, nipher, and TBRG are located in the open near the middle of the meteorological site, away from trees and obstructions.

In January 1993, a Campbell Scientific 21X data logger was installed by Environment Canada, which included a Fisher Porter weighing gauge as well as a HyQuest Solutions (HS) TB-3 TBRG. The logger was upgraded to a CS-23X on August 5, 2009 and to a CR3000 on November 2, 2011. These loggers, sensors and data belong to, and are maintained by, Environment Canada.

The publicly available data (Rawson Lake (AUT)) from the Environment Canada weather site is daily, from the CR3000 data logger and TBRG.

Currently, data loggers at the meteorological site include 1) a Campbell Scientific CR1000 data logger coupled to an HS TB-4 TBRG (in place since 31 July 2007), and 2) the CR3000 and TB-3 TBRG, mentioned above. Both data loggers record high-resolution data temporally and empirically. Data from these data loggers are recorded in mm. The TB-3 and TB-4 model TBRG record a tip event with each 0.2 mm of rain.

Historically, rain was measured in a copper standard gauge until August 1978. This rain gauge (and accompanying nipher graduated cylinder) measured precipitation in inches. Data within the database up to August 1978 have been converted to millimetres.

<u>Outlying rain gauges</u>

Outside of the meteorological site, there are currently four TBRGs and five SRGs located at five distinct locations in the ELA area. These rain gauge stations are referred to as RG3, RG21, RG22, RG24, and RG25. Stations RG24 and RG25 are equipped with a TB-3 and TB-4 TBRG, respectively, while RG3 and RG22 are each equipped with a WS525-R2 TBRG. All sites are also equipped with type B SRGs.

The TB-3 and TB-4 both record a tip event for every 0.2 mm precipitation, while the WS525-R2 records a tip event for every 0.254 mm precipitation.

Local locations and GPS coordinates of each currently active outlying gauge are as follows:
- RG3 (EIF gauge): Previously located down a ~300 m trail to the northeast of the EIF flume (GPS coordinates (WGS 84): UTM 15U E0448783, N5501312). Currently located across valley from the old location, up a ~ 200 m trail from the southern end of the EIF dike; GPS coordinates (WGS 84): UTM 15U E0448733, N5501174.
- RG21 (Chem Island): Located on the north side of the southern island on L240. GPS coordinates (WGS 84): UTM 15U E0447645, N5500068.
- RG22 (L375 gauge): Located east off Pine Road, about 300 m south of trail to L373. GPS coordinates (WGS 84): UTM 15U E0442575, N5510062.
- RG24 (L626 gauge): Located across Pine Road and towards L626 from the diversion channel. GPS coordinates (WGS84): UTM 15U E0442748, N5512081.
- RG25 (L260 gauge): Located on a corner of Pine Road between trails to L378 and L260. GPS coordinates (WGS84): UTM 15U E0444151, N5505139.

Outlying rain gauge data is not yet in the ELA database but is recorded and maintained by the HydroLim program. Other additional outlying gauges have been used in the past. For data or a list of past stations, please contact IISD-ELA through the data request platform.

Outlying TBRGs have used various brands of event loggers. All TBRGs collecting data up to and including the 2022 season utilized HOBO brand event loggers, except for the RG3 (EIF) TBRG. This station switched to a Solinst brand event logger in 2020. In 2022, the RG22 (L375) TBRG swapped to a TinyTag brand event logger after repeated failure of the HOBO logger.

All outlying TBRG event loggers were switched to TinyTag event loggers for the 2023 season.

TinyTag event loggers record number of tips per hour.

<u>Sample collection for chemical analysis</u>

As well as an SRG, station RG21 has a precipitation sample collector during the open water season, used to collect bulk precipitation samples for chemical analysis. Bulk precipitation sample collection is relocated to the metsite during the winter months to facilitate collection when ice is unsafe for travel.

The precipitation collector at RG21 consists of a square metal funnel which directs rainfall into a large plastic carboy. Photos and measurements of the precipitation collector are available by contacting Paul Fafard at <pfafard@iisd-ela.org>.

Historically, the winter bulk precipitation collector at the metsite consisted of an old CAPMoN precipitation bag inside a bucket open to the air 24 hours a day, 7 days a week. The precipitation bag was changed out once at least 20 mm of water equivalent precipitation had occurred.

As of fall 2018, an old CAPMoN automated precipitation collector has been used for winter bulk precipitation sample collection. This collector has a heated moisture sensor which uncovers the collection bag/bucket whenever precipitation is occurring. Once the sensor dries, the hood once again covers the sample to prevent evaporation and reduce contamination. Sample bags are changed after at least 20 mm of water equivalent precipitation has occurred.

<u>Limitations</u>

The standard type B rain gauge is easy to install, use, and maintain. That said, if precipitation isn’t completely emptied after each check, data for the following reading may be affected. The standard rain gauge is poor at collecting data when temperatures fall below 0 <sup>o</sup>C; if the nipher gauge is not used at or below 0 <sup>o</sup>C, data may be affected.

The nipher gauge is a large copper collector accompanied by a graduated cylinder calibrated to measure a “water equivalent” for the standard rain gauge. Due to the large surface area of the inside of the copper nipher, a film of water tends to cling to the nipher rather than empty into the water equivalent graduated cylinder. This may skew precipitation very slightly lower during the winter months.

Both the standard rain gauge and the graduated cylinder for the nipher are accurate to 0.1 mm of precipitation. Trace values are those which measure less than 0.1 mm.

Precipitation data collection has its own challenges due to normal weather phenomenon. When it is windy, rain can be blown across the top of collectors such as the standard rain gauge and therefore under-represent the true precipitation value. Alternately, snow from trees may be blown into the nipher on windy days when no new precipitation has occurred.

<u>Database information</u>

In the ELA database, units of measure are as follows:

- Time is Central Standard Time (CST) (GMT-6)
- Daily data based on total precipitation of climatological day
- Precipitation values were recorded in inches from 27 June 1969 to 31 July 1978, and have been converted to millimetres in the IISD-ELA database

Within the database, the meteorological site is identified as 239 AIR MET, where 239 is the lake centered location, AIR is the airshed sub-location of Lake 239, and MET is the station code. These codes are for the IISD-ELA maintained database only.

Each record contains the following data:

MEASURE_DATE is the field that contains the climatological date of each data record

RAIN is the field that contains the daily total precipitation value attributed to rain, in mm.

SNOW is the field that contains the daily total precipitation value attributed to snow, in mm.

TRACE is the field that contains a flag indicating trace values (\<0.1 mm) of precipitation. Use the following codes:

| **code** | **name** | **description** |
|----|----|----|
| T | trace | Trace precipitation. Non-specific historical code not in use any more |
| TR | trace rain | Trace rain. This is noted when trace precip was rain and measured daily value = 0, or when trace precip was rain and measured value was snow. E.g. daily total = 1.4 mm of snow, but TR noted at the previous evening check. |
| TS | trace snow | Trace snow. This is noted when trace precip was snow and measured daily value = 0, or when trace precip was snow and measured value was rain. E.g. daily total was 1.6 mm of rain, but TS noted at previous evening check. |
| TF | trace frost | Trace frost. No measurable precip occurred but trace noted due to frost. |
| TFR | trace freezing rain | Trace freezing rain. This is noted when trace precip was freezing rain and measured daily value = 0, or trace precip was freezing rain and measured value was snow or rain. E.g. daily total was 4.2 mm of snow but TFR noted at previous evening check. |
| MT | mixed trace | Trace mixed (rain and snow). This is noted when trace precip occurred as rain and snow, and measured daily value = 0 |
| TD | trace dew | Trace dew. This is noted when no measurable precip occurred but trace noted due to dew. |
| TH | trace hail | Trace hail. This is noted when trace precip occurred as hail and measured daily value = 0, or when trace precip was hail (or ice pellets) and measured value was rain or snow. E.g. daily total was 7.1 mm of rain but TH noted. |
| MIX | mixed precip | Mixed precipitation. This is noted when there is a mix of rain and snow (but can't estimate amounts of each) and total is more than trace. |
| FR | freezing rain | Freezing rain. This is noted when there is freezing rain that is more than a trace. |

<u>References</u>

http://publications.gc.ca/collections/collection_2012/ec/En56-238-3-2012-eng.pdf

ELA precipitation records

**<https://tinyurl.com/yb9jj7ou>** Government of Canada Weather Instruments tour page
