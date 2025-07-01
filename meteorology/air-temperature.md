# Air Temperature: Hydrometeorology Information Sheet

Update Date: 28 Jun 2023 (PF, added method code VT5, re-worded some areas)  
By: Paul Fafard, Ken Sandilands

# IISD-ELA Database Fields for Air Temperature:

Daily (Climatological Day)  
Location ID, Sublocation, Station ID  
Mean Date (YYYY-MM-DD)  
Maximum Temperature, Minimum Temperature (<sup>o</sup>C)  
Collection Method =VT1, VT4, VT5, AT1, AT2  
Data Set ID = M03  
Environment Canada public data for IISD Experimental Lakes Area found below:  
Rawson Lake (AUT): <https://tinyurl.com/ELAmetsite>

# General

Daily maximum and minimum air temperatures are two of several components measured at the IISD Experimental Lakes Area meteorological site, with the record beginning on June 26, 1969. The meteorological site has received instrumentation and support by Environment Canada since it was established. Publicly available data from Environment Canada instrumentation at the IISD-ELA meteorological station (called Rawson Lake (AUT)) is at the URL above.

Data that is collected, processed and analysed is utilized by a variety of research projects, scientists and graduate students from both within and outside of IISD-ELA. Many of the data sets are long term (now 50+ years) and provide understanding of natural variability in our ecosystems and will be valuable in future for studies such as climate change. They have proven invaluable in the planning of new experiments.

The majority of data in the daily maximum/minimum air temperature dataset was collected using manual read thermometers. From 2011-11-02 to 2017-11-20, data from manual thermometers and digital air temperature probes were being collected, and so these dates will have data from both methods. Since 20 November 2017, manual thermometers were discontinued and air temperature data is sourced from digital temperature probes.

# Site Location

The site is land based and is located 370 m west of Rawson Lake (L239), 400 m northwest of the field station, and 43 m above the lake surface.

UTM Coordinates  
15 U 0447128 5501551 (NAD83)  
15 U 0447138 5501331 (NAD27)  

# Collection Methods

<u>Climatological day</u>

All air temperature and precipitation data in the IISD-ELA database is based on the **climatological day** (for ELA, 8AM CST is used as the start of the climatological day) using the Meteorological Service of Canada’s definition of climatological day:

*Observations taken based on a calendar day cannot capture the minimums and maximums that are truly reflective of the peaks and lows over a 24-hour period. Normally, the coldest period in any given day is just before sunrise and the warmest period in a day is shortly after the sun reaches its zenith in the afternoon. A climatological day was therefore developed to ensure that the maximum and minimum temperatures could be captured. The climatological day tends to start and end at the same hour of two consecutive days. For example, the climatological day begins at the 0601 UTC observations on Day 1 and ends at the 0600 UTC observation on Day 2.*

*For sites that report two observations over a 24-hour period, MSC uses the following procedure to determine:*
- *Maximum temperature: For "today" is calculated from the maximum temperature reported for "today's" afternoon (PM) observation compared to the maximum temperature reported for "tomorrow's" morning (AM) observation;*
- *Minimum temperature: For "today" is calculated from the minimum temperature reported for "today's" morning (AM) observation and for "today's" afternoon (PM) observation;*
- *Rainfall, snowfall and precipitation totals: For "today" are calculated from "today's" afternoon (PM) observation with "tomorrow's" morning (AM) observation; and*
- *Snow on the ground: For "today" is based on "today's" morning (AM) observation.*

Daily thermometer checks occur twice per day; once at 08:00 CST and once at ~20:00 CST. The thermometers are read and reset at these times. Resetting a thermometer is simply moving the mercury or minimum rider bar to match the current temperatures.

Time periods for air temperatures in the IISD-ELA database are as follows:  
- Daily Maximum = Max temp during the 24hrs after 8AM on the date of the record.  
- Daily Minimum = Min temp during the 24 hrs before 8PM on the date of the record.  

E.g.
     
| August 26 |     | August 27 |     | August 28 |     |
| --- | --- | --- | --- | --- | --- |
| 08:00 CST | 20:00 CST | 08:00 CST | 20:00 CST | 08:00 CST | 20:00 CST |
| Max = 13.5 | Max = 22.5 | Max = 19.5 | _Max = **18.5**_ | Max = 14.0 | Max = 22.5 |
| Min = 9.5 | Min = 13.5 | _Min = **13.5**_ | Min = 14.0 | Min = 11.5 | Min = 14.0 |

The data in this table show that August 27 had a maximum temperature of 18.5 <sup>o</sup>C and a minimum of 13.5 <sup>o</sup>C. Maximum daily temperatures for August 27 are taken from the 08:00 – 08:00 period of August 27/28 and minimum temperatures are taken from the 20:00 – 20:00 period of August 26/27.

From 20 Nov 2017 onwards, CR1000 logger data is used in place of twice-daily manual thermometer checks. Minimum and maximum temperature data from the CR1000 is collected over the same time periods as the manual checks would have been (08:00 and 20:00). During spring, summer, and fall, temperatures are once again collected twice-daily using the thermometers. Data is coded to reflect collection method (see codes below, in Database Information section).

<u>Instrumentation</u>

For many years, the standard instrumentation for measuring air temperature at the ELA were manual read thermometers, housed in a Stevenson screen. The manual read thermometers consisted of two separate thermometers: one daily maximum thermometer and one daily minimum/current temperature thermometer. The maximum air temperature thermometer is a mercury thermometer, where the mercury advances as temperatures rise and will not retreat until it is reset by hand. The minimum/current air temperature thermometer is an alcohol thermometer with a minimum temperature indicator bar (a ‘rider’). The rider is pushed lower when the alcohol retreats as temperatures drop, and is left behind as the alcohol advances when temperatures rise.

These data make up the majority of the maximum and minimum daily air temperature dataset, extending from 1969 to late 2017. Since 20 November 2017, we have used digital temperature probes recording to data loggers as our primary source of air temperature data. In the event of missing data due to probe or logger malfunction, data from the Environment Canada datalogger is used to full gaps.

In January 1993, a Campbell Scientific 21X data logger was installed by Environment Canada, which included a Vaisala HMP 45C probe for air temperature. The logger was upgraded to a CS-23X on August 5, 2009 and to a CR3000 on November 2, 2011. These loggers, sensors and data belong to, and are maintained by, Environment Canada (currently named Environment and Climate Change Canada).

The publicly available data (Rawson Lake (AUT)) from the Environment Canada weather site is hourly or daily, from the CR3000 data logger and thermistor.

Currently, data loggers at the meteorological site include 1) a Campbell Scientific CR1000 data logger coupled to a Campbell Scientific HygroVUE 10 temperature and humidity probe (in place since 16 August 2022), and 2) the CR3000 and thermistor, mentioned above. Both data loggers record high-resolution data temporally and empirically. Data from these data loggers is in <sup>o</sup>C. The CR1000 and HygroVUE 10 combination is the current source of daily maximum and minimum air temperature data for the ELA database.

Historically, temperature has also been recorded using an analog chart recorder, though this data is not in the database at present and does not contribute to the daily maximum and minimum air temperature dataset.

<u>Limitations</u>

Mercury freezes at -39 <sup>o</sup>C. At this temperature, mercury within the thermometer will not move and will no longer give completely reliable data. Records exist with the ELA database below these temperatures; these records should be used with caution.

The T107C temperature probe has measurement limitation to between 50 <sup>o</sup>C and -35 <sup>o</sup>C. The Vaisala HMP 45C probe has a measurement limitation of -39.2 <sup>o</sup>C. The HygroVUE 10 sensor has a measurement limitation of -40 <sup>o</sup>C. Temperatures below these should be used with caution.

Data from the manually read/reset alcohol/mercury thermometers, and so has potential error due poor reading or incomplete reset. All data from the thermometers is rounded to the nearest 0.5 <sup>o</sup>C when read.

Data from digital probes is high quality, high resolution data, though potential error exists due to sensor drift between re-calibrations.

<u>Database information</u>

In the ELA database, units of measure are as follows:

- Time is Central Standard Time (CST) (GMT-6)

- Daily data based on maximums and minimums of climatological day

- Temperatures were recorded in <sup>o</sup>F from 26 June 1969 to 31 July 1978, and have been converted to <sup>o</sup>C in the IISD-ELA database

Within the database, the meteorological site is identified as 239 AIR MET, where 239 is the lake centered location, AIR is the airshed sub-location of Lake 239, and MET is the station code. These codes are for the IISD-ELA maintained database only.

Each record contains the following data:

MEAN_DATE is the field that contains the climatological date of each data record

MAX_TEMP is the field that contains the maximum daily temperature, in <sup>o</sup>C

MIN_TEMP is the field that contains the minimum daily temperature, in <sup>o</sup>C

COLLECTION_METHOD is the field that contains the code pertaining to the instrumentation used to collect the data

> VT1: Deployed from 26 June 1969 to 20 Nov 2017; the primary source of air temperature data over this time period. Data was recorded from readings of the maximum (mercury) and minimum (alcohol) thermometers within a Stevenson Screen at the ELA meteorological station (Environment Canada station ‘Rawson Lake’). Data from the thermometers is read to the nearest 0.5 <sup>o</sup>C.
>
> VT4: Deployed from 31 July 2007 to present; temperature data recorded digitally from the T107C thermistor and the CR1000 data logger at the ELA metsite. Data used as primary source of air temperature values between 20 November 2017 and 16 August 2022. This data also acts as back up for missing VT1 records and as a surrogate for VT5 data during HygroVUE sensor calibration. Data from the T107C thermistor is recorded to an accuracy of 0.01 <sup>o</sup>C. Timestamp for this data is in CST (GMT-6).
>
> VT5: Deployed from 16 Aug 2022 to present; temperature data recorded digitally from the HygroVUE 10 temperature and relative humidity sensor and CR1000 data logger at the ELA metsite. Data used as primary source of air temperature values since deployment. Data from the HygroVUE 10 has an accuracy of 0.1 <sup>o</sup>C between 20 and 60 <sup>o</sup>C, and 0.2 <sup>o</sup>C between -40 and 70 <sup>o</sup>C. Timestamp for this data is in CST (GMT-6).
>
> AT1: Air temperature data recorded on paper charts. Not in database at this point.
>
> AT2: Deployed from January 1993 to present; temperature data recorded from the HMP 45C onto the ECCC owned/operated CR3000 data logger at the ELA metsite. Previous data loggers coupled with the HMP 45C include a CS21X (January 1993 to August 5, 2009), a CS23X (until 2 November 2011). Timestamp for this data is in UTC (GMT-0), converted to CST if used to fill gaps in max/min dataset. Used to fill gaps only when VT4 is unavailable.

<u>References</u>

<https://www.campbellsci.com/107>; T107C range

<http://s.campbellsci.com/documents/us/manuals/hmp45c.pdf>; Vaisala HMP 45C range

<https://www.campbellsci.com/hygrovue10>; HygroVUE 10 range

http://publications.gc.ca/collections/collection_2012/ec/En56-238-3-2012-eng.pdf

ELA temperature records

<https://tinyurl.com/ydc75ux4> Sigma-Aldrich documentation on mercury

<https://tinyurl.com/ycy62se8> Government of Canada Weather Instruments tour page
