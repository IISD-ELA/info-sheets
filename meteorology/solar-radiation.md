# Solar Radiation: Hydrometeorology Information Sheet

Update Date: 22 June 2022 (KS); winter 2023/24 (KS); 15 April 2024 (PF)  
By: Ken Sandilands

# IISD-ELA Database Fields for Solar Radiation:

PAR (Photosynthetically Active Radiation)  
PAR_den - 15 min averages (µmol/s/m²)  
PAR_Tot - Totalized 15 min values (mmol/m²)  
Total Solar Radiation  
Hourly and 15 min averages (Watts/m^2)  
Totalized for hourly and 15 mins (KJoules/m^2)  
Bright Sunshine  
SunHours – 15 min and hourly totals (hrs)  
Environment Canada public data for IISD Experimental Lakes Area found below:  
Rawson Lake (AUT): <https://tinyurl.com/ELAmetsite>

# Site Location

The site is land based and is located 370 m west of Rawson Lake (L239), 400 m northwest of the field station, and 43 m above the lake surface. Altitude above sea level is 433m.

UTM Coordinates  
15 U 0447128 5501551 (NAD83)  
15 U 0447138 5501331 (NAD27)

# Collection Methods

Solar radiation is measured at the IISD-ELA metsite and recorded on a Campbell Scientific CR1000 datalogger which takes measurements every 5 seconds and calculates averages and totalizes as listed above. Solar radiation is measured continuously year round, however snow buildup on the sensors may affect readings. Snow is cleaned off the sensors daily during the morning metsite check (~ 08:00 CST ± 1 hour).

<u>Instrumentation</u>

PAR is measured with a Licor quantum sensor (LI-190R) connected to the data logger via a 604 ohm millivolt adapter (2290) and is calibrated every two years by Licor.

Total Solar Radiation is measured with a pyranometer (Kipp & Zonen SP Lite) and is calibrated every two years.

Bright sunshine (SunHours) is calculated by the CR1000 datalogger using the total solar radiation as a reference. Sun hours are calculated based on solar position which takes into account longitude and latitude, time of day, solar azimuth, solar elevation above horizon, declination, air pressure, air temperature, altitude, and air mass coefficient.

<u>Historical Data Collection</u>

<u>Total Solar Radiation</u>

Total Solar Radiation data start on 2012-11-09 there is no data prior to this date.

<u>PAR</u>

Over the years there have been several research groups/staff in charge of collecting the PAR data at the metsite, which has resulted in datasets collected with differing units, intervals, and sensors.

As of 2008-10-16 the PAR sensor has been on a CR1000 Campbell Scientific datalogger, and collected consistently at 15 min intervals, continuously (year-round, and during the night), with units of µmol/s/m². Since this setup, the data are more reliable, and there are no time shift issues.

Prior to 2008-10-16, it isn’t clear who collected the PAR data, and how it was collected. Likely a Licor sensor was used paired with a Licor datalogger. PAR data starts on 1973-04-15 and was only collected during daylight hours during the open water seasons. From 1973 to 1982 it appears that perhaps only a maximum daily PAR value was recorded and the data are fitted equally on each side of the daily maximum, as each day has uniform raise and fall but with differences in peaks between days:

<img src="./attachments/media/image1.png" style="width:7.08333in;height:3.66667in" />

Starting in 1983, it appears that there are true 30min values since the daily plot of the values is not always raising and falling at a constant rate:

<img src="./attachments/media/image2.png" style="width:7.08333in;height:2.80208in" />

It is assumed that the 30 min data starts in 1983 as the peaks are no longer uniform and prior to this, the data are only daily maximums.

<u>Time drift problems</u>

Prior to 2008 there are parts of the data where it appears that there have been some time drift problems, which could be due to errors, mismatch between dataloggers and download computers, equipment mistakenly set to DST instead of CST, and time drift of early dataloggers. Parts of these data have been adjusted using the clock drift tool in Aquarius Time Series software in an attempt to line up the data with solar noon for Kenora as provided by NRC for the entire period. These time corrections are tricky as it isn’t possible to line up the peak daily PAR with solar noon on cloudy days, and it is difficult to determine when a block of data needs to be started/ended due to cloudy days. For a list of time corrections made to the data, see Appendix 1.

**Appendix 1**

|  | **Category** | **Type** | **Processing priority** | **Comment or Note** | **Start** | **End** | **Created** | **Created by** | **Tags** |
|----|----|----|----|----|----|----|----|----|----|
|  | Correction | Override | Normal | Override: Clock Drift‌ Start offset: 60:00.‌ End offset: 60:00.‌ | 2004-05-05 16:00:00 | 2004-06-07 19:00:00 | 2023-12-01 10:13:59 | Julie |  |
|  | Correction | Override | Normal | Override: Clock Drift‌ Start offset: 30:00.‌ End offset: 30:00.‌ | 2003-09-18 06:00:00 | 2003-10-06 17:30:00 | 2023-12-01 10:10:02 | Julie |  |
|  | Correction | Override | Normal | Override: Clock Drift‌ Start offset: 30:00.‌ End offset: 30:00.‌ | 2003-07-19 04:00:00 | 2003-09-04 18:30:00 | 2023-12-01 10:08:27 | Julie |  |
|  | Correction | Override | Normal | Override: Clock Drift‌ Start offset: 30:00.‌ End offset: 30:00.‌ | 2003-06-23 03:30:00 | 2003-07-02 20:00:00 | 2023-12-01 10:06:25 | Julie |  |
|  | Correction | Override | Normal | Override: Clock Drift‌ Start offset: 30:00.‌ End offset: 30:00.‌ | 2003-06-14 03:30:00 | 2003-06-20 18:30:00 | 2023-12-01 10:05:16 | Julie |  |
|  | Correction | Override | Normal | Override: Clock Drift‌ Start offset: 30:00.‌ End offset: 30:00.‌ | 2003-06-10 03:30:00 | 2003-06-10 20:30:00 | 2023-12-01 10:04:23 | Julie |  |
|  | Correction | Override | Normal | Override: Clock Drift‌ Start offset: 30:00.‌ End offset: 30:00.‌ | 2003-05-22 04:00:00 | 2003-05-22 20:00:00 | 2023-12-01 10:03:19 | Julie |  |
|  | Correction | Override | Normal | Override: Clock Drift‌ Start offset: 30:00.‌ End offset: 30:00.‌ | 2003-01-13 07:30:00 | 2003-01-27 16:30:00 | 2023-12-01 09:58:02 | Julie |  |
|  | Correction | Override | Normal | Override: Clock Drift‌ Start offset: 60:00.‌ End offset: 60:00.‌ | 2003-01-11 07:00:00 | 2003-01-12 16:00:00 | 2023-12-01 09:57:26 | Julie |  |
|  | Correction | Override | Normal | Override: Clock Drift‌ Start offset: 30:00.‌ End offset: 30:00.‌ | 2003-01-10 07:30:00 | 2003-01-10 16:30:00 | 2023-12-01 09:57:01 | Julie |  |
|  | Correction | Override | Normal | Override: Clock Drift‌ Start offset: 30:00.‌ End offset: 30:00.‌ | 2002-11-22 07:30:00 | 2002-12-02 16:00:00 | 2023-12-01 09:55:18 | Julie |  |
|  | Correction | Override | Normal | Override: Clock Drift‌ Start offset: 30:00.‌ End offset: 30:00.‌ | 2002-10-31 07:00:00 | 2002-11-10 16:30:00 | 2023-12-01 09:54:16 | Julie |  |
