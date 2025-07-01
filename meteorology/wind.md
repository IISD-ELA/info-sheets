# Wind: Hydrometeorology Information Sheet

Author: Ken Beaty, Ken Sandilands, Paul Fafard  
Last Update: March 26, 2020 (PF); October 2020 (KS); March 22, 2022 (PF)

# IISD-ELA Database Fields for Wind

Location, Sublocation, Station  
Data Set ID = M07  
Collection Method (WD1, WD2, WD3, WD4, WD5, WD6)  
Measure Date (YYYY-MM-DD)  
Hour (CST)  
Direction Degrees  
Speed Measured (km/h)  
Speed at 10 m (km/h)  
Instrument  
Tower Height  
Environment Canada public data for IISD Experimental Lakes Area found below:  
Rawson Lake (AUT): <https://tinyurl.com/ELAmetsite>

# General

Wind data is one of several components measured at the Experimental Lakes Area (ELA) meteorological site with record beginning in June 1969. The site was established by Environment Canada, Meteorological Service (MSC) who provided instrumentation and technical support in all years. Site service and data abstraction have been provided by ELA within the envelope of the Hydrology Program (currently, HydroLim). Data are stored in the ELA database as well as being routinely submitted to the MSC Ontario Climate Centre in Downsview, Ontario under the name “Rawson Lake Station”. For a site description and discussion of components see Beaty and Lyng (1989).

A second data logger owned by ELA was installed initially to replace a LICOR logger that had been dedicated to PAR solar radiation data. This new logger, a Campbell Scientific model CR-1000, was installed on July 31, 2007 and while initially intended for light data, was gradually expanded to include other sensors that eventually included wind, barometric pressure, temperature, relative humidity, and precipitation. The programing code for wind speed and direction was added on June 24, 2008. An RM Young anemometer was mounted on the communication tower at the MET Site at 10 m above ground. This set-up is owned and maintained by ELA.

# Site Location

The site is land-based and is located 370 m west of Rawson Lake (L239), 400 m northwest of the field station and 43 m above the lake surface.

UTM Coordinates  
15 U 0447128 5501551 (NAD83)  
15 U 0447138 5501331 (NAD27)

# Collection Methods

<u>Units of measure</u>

In the ELA database, units of measure are as follows:
- Time is central standard time (CST).
- Hours are “hour ending” (i.e. hour 2 is the end of the second hour)
- Mean wind speed is kilometres per hour (km/h) calculated for the hour.
- Maximum wind speed (also km/h) recorded over the hour.
- Mean vector magnitude for the hour (use of the mean wind vector magnitude is not recommended for straight-line Gaussian dispersion models but may be used to model transport direction in a variable-trajectory model).
- Wind direction is the prevailing direction in degrees true north from which the wind is blowing. Instrumentation changed in 1993 and a more thorough discussion is provided under the next two discussion sections.
- Standard deviation of wind direction calculated using Campbell Scientific's wind speed weighted algorithm.

<u>Instrumentation</u>

The standard instrument for measuring wind is the anemometer. To date, two types of anemometers have been used at ELA: the type 45B anemometer, with analog chart recorder, and the RM Young anemometer, with a digital Campbell Scientific data logger (CS-21X from January 3, 1993 to August 5, 2009; CS-23X from August 5, 2009 to November 2, 2011; CR-3000 from November 2, 2011). This equipment is owned by Environment Canada.

From the beginning of record to January 12, 1993 the type 45B anemometer was used. It consists of three conical cups mounted with a directional vane and was wired to an anemograph recorder with a daily chart. Each mile of wind passing and its direction were simultaneously recorded on completion. Charts were hand-scaled to provide hourly wind speed (number of miles completed during the hour) and prevailing direction during the hour recorded to the 8 points of the compass. The prevailing direction was determined by occurrence within the hour. The wind direction is the direction from which the wind is blowing and is given as the true bearing rather than magnetic. Directions were converted to degrees for the database where:

> N = 360<sup>o</sup> NE = 45<sup>o</sup> E = 90<sup>o</sup> SE = 135<sup>o</sup>
> S = 180<sup>o</sup> SW = 225<sup>o</sup> W = 270<sup>o</sup> NW = 315<sup>o</sup>

The unit of measure for wind speed was miles per hour with the Type 45B and values were converted to kilometres per hour (km/h) for the ELA Database.

A problem of directional bias in favour of the non-cardinal (NE, NW, SE, SW) wind directions is inherent in the MSC Type 45B wind equipment. Koren (1971) evaluated the problem and suggested that this bias is due to the relatively long lag time interval during which the wind direction is sampled. Users are cautioned that the directions presented here should be used in a general manner only and not be interpreted as being exact.

From January 13, 1993 to present, a RM Young anemometer was installed. The wind speed sensor is a four-blade helicoid propeller with directional vane connected to a Campbell Scientific 21X data logger. The software used is the MSC national program that records several meteorological components and stores the data using Universal Time Standard (UTC) for time, knots for speed and degrees for direction. All data has been corrected to CST, km/h and degrees for the ELA database. The determination of hourly speed and direction for the RM Young is different than for the Type 45B and is discussed more fully below.

<u>Detection limits</u>

1)  Prior to January 13, 1993

> Prior to January, 1993 wind speed was recorded to the nearest whole mile per hour. Data was converted to kilometres per hour and entered into the Database to the nearest 0.1 km/h. Speed is the total or cumulative amount for the hour ending as indicated (HOUR field). Therefore, an entry of zero means that there was cumulatively 0 miles of wind for the entire hour.
>
> Direction was recorded as the prevailing direction within the hour to one of the eight cardinal points. For example, during an hour in which 10 miles of wind passed the anemometer, each mile would have a direction assigned to it on completion. If it recorded SW 6 times and NW 4 times, then the prevailing direction was said to be SW at 10 miles per hour. For the Database, these directions were converted to discrete values in degrees, with North being 360<sup>o</sup> (not zero degrees).
>
> b\) January 13, 1993 to present
>
> The data logger records velocity to the nearest 0.00001 knot. Hourly values reported in the Database were averaged from 5 s readings within the hour, converted from knots and stored to the nearest 0.1 km/h. Therefore, speeds up to 0.04999 are stored as zero.
>
> Hourly direction values reported in the Database were averaged from 5 s values to the decimal of a degree for the hour. Values were rounded to the nearest 0.1 degree for the Database where 360<sup>o</sup> represents true north (there is no 0<sup>o</sup> direction) and the first reported value for the circle is 0.1 degrees.

3)  Consideration for calm periods and directional bias

> Due to the inherent differences in the two types of equipment used, users are cautioned as to their treatment of periods of calm or low wind speed as well as the reported precision of direction data.
>
> d\) Missing Record:
>
> In the Database, periods of missing speed or direction were indicated as blank or “null” data. It is important to understand that a wind speed of zero is data but that a blank entry means “missing” or “not available”.
>
> Digital wind sensing and logging instruments are sensitive to damage from electrical storms and surges that may result in false values being recorded. All attempts have been made to identify and remove erroneous data and store such periods as “null” data.

<u>Height of exposure</u>

Wind anemometers are normally exposed at a height of 10 m. The wind tower erected in 1969 had a height of 12.2 m (40 feet) because of the nature of the forest canopy surrounding the site. On May 20, 1986, the tower was relocated 50 m to the SW and replaced with a 10 m pivoting arm tower to eliminate possible interference with nearby precipitation chemistry and air quality sampling equipment. The tower height since that time has been consistent with the internationally accepted height for exposure of wind instruments.

A method for vertical height correction is provided by Buckler (1969) as follows:

> V<sub>1</sub> / V<sub>2</sub> = (Z<sub>1</sub> / Z<sub>2</sub>)<sup>p</sup> where:
>
> V<sub>1</sub> = mean speed at height Z<sub>1</sub>
>
> V<sub>2</sub> = mean speed at height Z<sub>2</sub>
>
> p = exponent that varies with terrain (0.14 – 0.50); assumed 0.25 for ELA

<u>Forest fire history</u>

Two major forest fires in 1974 and 1980 have severely impacted the forest in the Rawson Lake Watershed and may have influenced the wind record due to altered exposure and terrain roughness. The 1974 fire burned only the eastern half of the watershed, however, the 1980 fire burned almost the entire catchment and the area surrounding the meteorological station. From 1969 until the 1980 fire, the site was surrounded by a mature mixed forest of predominantly pine, spruce, birch and poplar. The fire consumed all needles and most small branches as well as all ground cover. Over the 3-4 year period that followed, most of these trees had fallen down and a thick, young Jack Pine forest was well established. By the fall of 1988, nearly all of the old forest was down. Occasional measurements of tree height were made on the four sides of the site. Averages and the range of measured values are as follows:

> <u>Year</u> <u>Average</u> <u>Range</u>
>
> 1969 to 1980 13 m 10 – 15 m
>
> 1988 2.8
>
> 1989 3.0 2.1 – 4.0
>
> 1990 4.1 3.6 – 4.6
>
> 2004 6.4 5.3 – 7.2
>
> 2020 10m not specifically measured, same height as 10m anemometer

<u>Wind over water</u>

It is important to consider that the wind reported in the database is monitored from a land based station and may be unlike that occurring directly over ELA lakes. Solinske (1982, unpublished report) addressed this problem as being the result of variability in fetch, atmospheric stability and topographic roughness. His study investigated the correlation of the wind speed measured at the meteorological station to wind data collected at the centre of three lakes of varying size (L239, L223 and L470). Solinske demonstrated clearly that at ELA, fetch plays an important roll influencing the amount of wind that the lake receives. Moore (1996, unpublished report) expanded this study by developing correlations of wind speed between the meteorological station and lakes 239 and 979. Moore determined that the wind at lakes 239 and 979 were 82% and 70%, respectively, of that recorded at the meteorological station.

<u>Description of the data set in the database</u>

This data set contains hourly wind speed and hourly prevailing direction as described above.

In the ELA database, the site is identified as 239 AIR MET, where L239 is the lake-centred location, AIR refers to airshed sublocation of Lake 239, and MET is the station code.

Each record contains the following data:

> HOUR is the field for the hour ending (i.e. HOUR = 1 is the period from 1 s after mid-night to 01:00).
>
> TOWER_HT is the data field that states the height of the tower (i.e. instrument height above ground) in metres.
>
> SPD_MEAS is the field that contains the measured wind speed in km/h.
>
> SPD_10M is the field that contains the wind speed adjusted to 10 metres above ground if it had been collected at a height other than 10 m. Wind direction is assumed not to be affected by tower height.
>
> INSTRUMENT_TYPE = WD# is a method code to describe the equipment and tower height for each value where:
>
> WD1: From June 28, 1969: anemometer type MSC 45B; tower height 12.2 m; hand scaled chart record; speed measured in miles per hour converted to km/h; direction to 8 cardinal points converted to whole degrees; Central Standard Time (CST).
>
> WD2: From May 19, 1986: anemometer type MSC 45B; tower relocated 50 m SW and upgraded to a pivoting arm tower; height 10 m; speed measured in miles per hour converted to km/h; direction to 8 cardinal points converted to whole degrees; Central Standard Time (CST).
>
> WD3: From January 13, 1993: anemometer type RM Young; Campbell Scientific 21X data logger; tower height 10 m; hourly output; speed measured in knots converted to km/h; direction in degrees; Universal Time Standard (UTC) was converted to Central Standard (CST).
>
> WD4: This RM Young (Campbell Scientific 05103-10) anemometer is mounted at a height of 10 m on the communication tower, hourly output in km/h, direction in degrees, CST, data collected on a Campbell Scientific CR-1000 mentioned on page 1. Hourly mean wind vector magnitude, and standard deviation of wind direction are also calculated and recorded by the CR-1000. As of September 2017, this data is only used as a backup for when the WD5 data is not available. *AQUARIUS Grade Code: 11*
>
> WD5: From November 2, 2011(ECCC anemometer): anemometer type RM Young; Campbell Scientific CR-3000 data logger; tower height 10 m; hourly output; speed measured in m/s converted to km/h; direction in degrees; Universal Time Standard (UTC) was converted to Central Standard (CST); owner of equipment was EC.Tree height assessed in 2020, resulting in this site as a Class 5. *AQUARIUS Grade Code: 8*
>
> WD6: Oct 28,2020 Newly calibrated RM Young anemometer (IIS-ELA’s) mounted relocated on new 10m tower at the middle of the metsite further from the trees and connected to CR1000 as with WD4. This relocation of wind tower improved the Class of the site from a 5 to a 4. See p.18 MSC Automatic Weather Station Configuration Manual.
>
> *AQUARIUS Grade Code: 10*

<u>References</u>

Beaty, K.G., and M.E. Lyng. 1989. Hydrometeorological data for the Experimental lakes Area, northwestern Ontario, 1982 to 1987. Can. Data Rep. Fish. Aquat. Sci. 759: v + 280 p.

Buckler, S.J. 1969. The vertical wind profile of monthly mean winds over the prairies. Canada Department of Transport. Meteorological Branch. Tech. Report \#718.

Koren, O. 1971. Evaluation of the directional bias in the M.S.C. type 45B wind system. Can. Dep. Transport Tech. Memo. Rep. 8.

Solinske, A. 1982. Analysis and prediction of overwater windspeeds on three small lakes in the Precambrian Shield. B.A. Honours Thesis submitted to the Department of Geography, University of Winnipeg. Unpublished.

Moore, R. 1996. The analysis and prediction of wind speeds over water. Student Co-op Work Term Report. Unpublished.
