# Ice Phenology Information Sheet

**Authors**: Ken Beaty, Ken Sandilands, Paul Fafard, Chris Hay, Scott Higgins, Delvin So  
**Last Updated**: 2025-06-16  
**Last Updated By**: Delvin So  

## Contents
- [General Information](#general-information)
    - [Background of the Dataset](#background-of-the-dataset)
    - [Lake Size vs. Ice Phenology Relationship](#lake-size-vs-ice-phenology-relationship)
    - [Significance to IISD-ELA, and Research Applications](#significance-to-iisd-ela-and-research-applications)
    - [Predicting Ice-on and Ice-off](#predicting-ice-on-and-ice-off)
- [Data Dictionary](#data-dictionary)
    - [Tables and Lists of Columns](#list-of-columns)
        - [Ice Phenology - Table info and columns](#ice-phenology---table-info-and-columns)
        - [Ice Watch - Table info and columns](#ice-watch---table-info-and-columns)
    - [Column Definitions](#column-definitions)
        - [Ice Phenology - Column Definitions](#ice-phenology---column-definitions)
        - [Ice Watch - Column Definitions](#ice-watch---column-definitions)
    - [Parameter Definitions](#parameter-definitions)
- [Methods](#methods)
    - [Method Codes](#method-codes)
    - [Ground-based visual observations ICE1](#ground-based-visual-observations-ice1)
        - [Ice-Off](#ice-off)
        - [Ice–On](#iceon)
        - [Vantage Points](#vantage-points)
    - [Trail cameras and satellite imagery ICE2](#trail-cameras-and-satellite-imagery-ice2)
- [References](#references)


## General Information

### Background of the Dataset

Ice phenology refers to the duration of ice cover on a seasonally ice-covered lake. The longest and most continuous (1969 – present) record of ice phenology at the IISD Experimental Lakes Area (IISD-ELA), is from Lake 239 (also called “Rawson Lake”).

Historically, it has been very important for individuals to be present at IISD-ELA during the two “shoulder seasons” (spring ice-off and fall ice-on) to collect visual ice observations of Lake 239. In those shoulder seasons, the population of the field station typically numbered between 1 to 4 persons, so we are indebted to the care taken by those personnel.

In more recent years, newer methods (trail cameras and satellite imagery) have been used, and other IISD-ELA lakes besides Lake 239 have been surveyed to collect data for ice-on and ice-off dates on an ad hoc basis. IISD-ELA continues to explore ways to grow this dataset into the future.

### Lake Size vs. Ice Phenology Relationship

Historically, Lake 239 ice phenology records served as a qualitative index of the ice-on or ice-off dates for other regional lakes. More recently, Higgins et al. (2021) evaluated the role of climate and lake size in regulating ice phenology in the IISD-ELA region. They found that lake size plays an important role in the timing of ice-on and ice-off dates and the total duration of ice-cover. In general, as lake size increases ice-on dates occur later due to the larger heat budgets and longer time required for the lakes to cool. During the spring, ice-off dates also occur later as lake size increases even for lakes near each other. This appears to occur because the larger fetch of large lakes increases the over lake wind speeds and ‘pushes’ snow to the ‘downwind’ edges of the lake. Snow is an excellent insulator, and the reduced snow cover on larger lakes leads to the development of thicker ice that takes longer to melt in the spring.

Overall, for lakes with surface areas between 0.2 – 10 km<sup>2</sup> (20 – 1000 ha) the difference in ice-on dates is, on average, 30 to 45 days (i.e. the largest lakes become ice-covered 30-45 days after the smallest lakes). During the spring, the difference is smaller with the ice-off dates for the largest lakes occurring, on average, 10-21 days after ice-off on the smallest lakes. Overall, the difference in the duration of ice-cover is, on average, 22-38 days across the range in lake size.

For information on the size, depth, and volume of Lake 239 and other nearby lakes, please consult the most recent version of our IISD-ELA bathymetry data package: <https://portal.edirepository.org/nis/revisionbrowse?scope=edi&identifier=1276> (as of writing, IISD Experimental Lakes Area 2025).

### Significance to IISD-ELA, and Research Applications

A quantitative understanding of ice-phenology at the ELA has proved useful. Logistically, spring sampling occurs as soon as possible after ice-off so visual observations of ice-break up and communication to offsite staff, including LTER staff and research, has served a very practical and immediate purpose.

Given the strong role of air temperature in modulating ice-on and ice-off dates, changes in ice-phenology over time (e.g. decadal or longer) is a quantitative indicator of climate change. As noted by Higgins et al. (2021) over the 1970-2019 period the duration of ice-cover on L239 has declined by c. 4 days per decade, or approximately 3 weeks over the 50+ year period.

The duration of the ice-free period also has implications for lake heating, the timing of stratification, gas exchange and annual evaporation. These may be important considerations for other research on seasonally ice-covered lakes.

### Predicting Ice-on and Ice-off

> *“In my opinion, it doesn’t matter how cold the winter was or how thick the ice. The only thing that matters is the weather in the last two weeks of April.”*
>
> \- Barney Lamm, Ball Lake Lodge founder (Lake of the Woods News 2000)

The close proximity of Lake 239 to ELA’s meteorological station has also allowed the development of models that predict ice-on and ice-off events based on air temperature. The models align closely with the quote of Barney Lamm (above) who predicted that ice-off dates on Lake 239 have been primarily driven by ‘recent’ air temperatures. In general, the ice-off date has generally occurred between 24 – 27 days after the 31-day running average of air temperature rose above 0 degrees Celsius.

More recently, IISD-ELA have combined long-term ice phenology data with meteorology and limnology datasets to predict ice-off using machine learning. A model was developed and first used to predict ice-off in 2024, with reasonably good accuracy. As of writing, it is under further testing and development, so it has not yet been released publicly.

## Data Dictionary

### Tables and Lists of Columns

Key columns (compound keys) are indicated with asterisks (\*).

#### Ice Phenology - Table info and columns
Table name: `lim_ice_dates_obs_annu_manu`  
This is the main table with the most important information: ice-on, ice-off, and duration of ice season.
<p style="margin-bottom:0">List of columns:</p>

- dataset_name
- monitoring_location_name\*
- characteristic_name\*
- activity_start_date\*
- activity_end_date
- result_value
- result_unit
- method_sample_code
- result_comment
- update_date

#### Ice Watch - Table info and columns
Table name: `lim_ice_watch`  
This is a newer table (2024 onward) based on a field form used to obtain more detailed "raw" metadata surrounding each ice observation.
<p style="margin-bottom:0">List of columns:</p>

-	dataset_code
-	record_key*
-	date
-	time
-	observer
-	observer_other
-	monitoring_location_name
-	observation_point
-	wind_dir
-	weather_condition
-	visibility
-	ice_cover_type
-	ice_cover_pct_est
-	notes_ice_edge
-	notes_refreeze_rethaw
-	season_ice_phen
-	comments
-	lon_dd
-	lat_dd
-	photo_name
-	photo_direction
-	quality_issue_flag
-	quality_issue_comment
-	update_date
-	account
-	version

### Column Definitions

#### Ice Phenology - Column Definitions

 Column name (alphabetical) | data type | unit| definition 
----------------------------|-------------------|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 activity_end_date  | date      | day | For ice on or ice off rows this is left empty. For ice duration rows this is the associated ice off date.
 activity_start_date        | date      | day | For ice on or ice off rows this is the associated date. For ice duration rows this is the associated ice on date.   
 characteristic_name        | character varying | N/A                 | The parameter being measured. For ice phenology, ice on, ice off, or ice duration. 
 dataset_name       | character varying | N/A                 | Name of the dataset. A dataset is a collection of data to which several individual data records (rows) belong. Dataset names are useful to distinguish groups of data across different research fields and provide some descriptive context.     
 method_sample_ code     | character varying | N/A                 | A short and unique code associated with a description of a method of sampling for data (i.e., how the physical sample was collected or measured in the field). A key to look up descriptions for codes should be included with the associated Information Sheet for the dataset in question.       
 monitoring_location_name   | character varying | N/A                 | Name of sampled or surveyed geographic location at the IISD Experimental Lakes Area field site. The name consists of: &lt;location&gt; or &lt;location sublocation&gt; or &lt;location sublocation station&gt;. Location is typically the lake number (each lake is named with a number, representing the lake's geographical watershed), sublocation which typically specifies LA for "lake" (or a basin, e.g. NB - north basin, or other), and station which is usually CB ("centre buoy" - at about the deepest point of the lake). Some names do not have all three parts since a broader area is in question (e.g. for bathymetry, the entire lake, not just the centre buoy). 
 result_comment     | character varying | N/A                 | Remarks about the record or its collection. For ice phenology, this includes information about re-freeze or re-thaw events, which can be used to modify ice on, ice off, and ice duration to fit different definitions.    
 result_unit        | character varying | N/A                 | Units of measure for the result value, associated with the characteristic name parameter.  
 result_value       | numeric   | variable - see column "result_unit" | The result value for the characteristic name in question. Basically, this is the meaningful number measured or determined for the parameter in question. This column is usually used for long-form (vs. wide) data tables.        
 update_date        | date      | day                 | Date the record in the IISD-ELA Postgres Master Database table was uploaded to the database or most recently modified. Format: YYYY-MM-DD.       
<br>

#### Ice Watch - Column Definitions

| column name               | data type           | unit   | definition |
|---------------------------|---------------------|--------|------------|
| dataset_code              | varchar(3)          |        | Three letter code for each dataest found in the ref_dataset table.      |
| record_key                | uuid                |        | A unique ID to identify that observation, coming from the Survey123 form.      |
| date                      | date                |        | The date the observation was made, YYYY-MM-DD.        |
| time                      | time                |        | The time the observation was made, HH:MM:SS.          |
| observer                  | varchar(100)        |        | The name of the obesrver.      |
| observer_other            | varchar(100)        |        | The name of the other observer.      |
| monitoring_location_name  | varchar(62)         |        | Name of sampled or surveyed geographic location at the IISD Experimental Lakes Area field site. The name consists of: <location> or <location sublocation> or <location sublocation station>. Location is typically the lake number (each lake is named with a number, representing the lake's geographical watershed), sublocation which typically specifies LA for "lake" (or a basin, e.g. NB - north basin, or other), and station which is usually CB ("centre buoy" - at about thedeepest point of the lake).                                          |
| observation_point         | varchar(100)        |        | The specific area near the lake at which the observation was made.            |
| wind_dir                  | varchar(32)         |        | Direction of the wind determined by a compass arrow into the wind. This can also be recorded as 'calm'. |
| weather_condition         | varchar(100)        |        |  A mark on the weather condition at the time the observation was made.    |
| visibility                | varchar(32)         |        |  A remark on the visibility of the lake at the time the observation was made.            |
| ice_cover_type            | ice_cover_enum      |        |  A categorization of how much ice covered the lake, if any. This can be one of   open, partial, or complete.        |
| ice_cover_pct_est         | smallint            | %      |  An estimate of how much ice covered the lake, if any.         |
| notes_ice_edge            | varchar(255)        |        |  Notes made regarding the edge of the ice at the time of observation, such as whether there is snow, open water, and so on.      |
| notes_refreeze_rethaw     | varchar(255)        |        |  A note made regarding the season (fall/spring), and the lake's previous and current status.          |
| season_ice_phen           | varchar(30)         |        |  The year concatenated with 'ice-on', 'ice-off', or 'indetemrinate'. This is useful for data users to join this table with other ice phenology tables, such as lim_ice_dates_obs_annu_manu, in conjunction with monitoring_location_name.          |
| comments                  | varchar             |        |  Remarks made about the record or its collection.          |
| lon_dd                    | double precision    | °      |  The longitude, in degrees, of where the observation was made.      |
| lat_dd                    | double precision    | °      |  The latitude, in degrees, of where the observation was made.         |
| photo_name                | varchar             |        |  The name of the photo taken during the observation. Currently not exported with the rest of the Survey123 data.           |
| photo_direction           | varchar             |        |  The direction of the photo taken during the observation. Currently not exported with the rest of the Survey123 data.               |
| quality_issue_flag        | boolean             |        | A boolean, True indicates a quality issue, otherwise False. If set to True, 'quality_issue_comment' should also be filled out.           |
| quality_issue_comment     | varchar             |        | Remarks pertaining to the quality of the observation.           |
| update_date               | date                |        | The date the record was inserted or updated in the table. YYYY-MM-DD            |
| account                   | varchar(30)         |        | The username of the individual responsible for the insert or update.         |
| version                   | smallint            |        | Defaults to 1, incremented by 1 for each update made thereafter.        |
<br>

### Parameter Definitions

| **characteristic_name (alphabetical)** | **definition** |
|----|----|
| Day, ice off | The date of the beginning of the lake being ice-free (melted or thawed out). We define ice-off date as the last date when 80% or more of the lake surface is ice-free. For more information, please consult the method code definitions in the methods section of the ice phenology info sheet. |
| Day, ice on | The date of the beginning of the lake being frozen over with ice. We define ice-on date as the first date when 80% or more of the lake surface is ice-covered. For more information, please consult the method code definitions in the methods section of the ice phenology info sheet. |
| Ice cover duration | The number of days the lake was ice covered for the winter of the records in question. This is calculated for each winter season (which always runs across two calendar years at IISD-ELA) as later date (ice-off in the spring of the next year) minus earlier date (ice-on in the fall of the previous year). Note that leap years are carefully accounted for in these calculations, as February occurs in the winter season (ice-covered season) for IISD-ELA. |

## Methods

### Method Codes

It is worth noting that, at this time, there is no global standard for defining ice phenology, so it is important for data users to read the definitions provided with each dataset and for data providers to remain consistent (or note any inconsistencies) in the methods used to collect the data (Sharma et al., 2022). Therefore, we outline the two methods we have used to determine ice-on and ice-off dates, and they are specified for each data record with a code. The main distinction between our two codes is the observation method: ground-based in-person (ICE1) or via trail cameras and satellite imagery (ICE2).

| **code** | **short description** |
|----|----|
| ICE1 | Ice phenology based on in-person observations. We define ice-on (off) date as the first (last) date when 80% or more of the lake is ice-covered (ice-free), and ice duration as the difference. Re-freeze and re-thaws are noted in the comments when they occur. |
| ICE2 | Ice phenology based on trail cams and sometimes also satellite or in-person observations. We define ice-on (off) date as the first (last) date when 80% or more of the lake is ice-covered (ice-free), and ice duration as the difference. Re-freeze and re-thaws are noted in the comments when they occur. |

### Ground-based visual observations (ICE1)

The dates for ice-on and ice-off are based on the judgement of an observer who looks over the lake from a vantage point and estimates the presence of ice visually. These observations generally happen more frequently when it is observed that breakup is about to occur or that the lake is getting close to freezing. Observations are made in the morning after sunrise and again before sunset, by recording an estimate of the ice cover as a percentage.

#### Ice-Off

The date of "ice -off" is defined as being the last date on which 80% or more of the ice has melted. The ice usually melts quickly within a day or two once the "candled" ice sheet has broken up. Most often, on the last day of ice cover, the blackened candled ice will cover the entire lake in the morning and, over the course of the day, completely disappear by late afternoon or early evening. This date has usually been fairly easy to quantify. In rare cases of where the lake freezes and thaws again, the last thaw date is taken and the alternate date is noted in the comments.

#### Ice–On

The date of “ice-on” is defined as the first date where the lake is 80% or more ice covered. The precise date for ice-on is generally more difficult to quantify than ice-off, since the formation of thin ice-layers may be subsequently broken up by wind induced turbulence. Considering the original use for the data, it was usually adequate to know when the lake was “effectively ice covered” and was defined as the first date that the ice cover had reached 80% or greater. In most years when applicable, both the 80% and 100% dates were recorded if freezing was gradual, however the 80% frozen date is used as the official date for consistency. The date on which ice first appeared along shorelines and small bays was not normally recorded. Typically, the main body of the lake freezes over all at once in one night. However, in some years, the lake freezes gradually, resulting in a partial ice sheet for a varying number of days before completely freezing over. This was the case in at least two ice-on dates (2009 and 2015) on record. The following field notes illustrate three examples of typical situations.

Field notes: 
- Nov 26, 2009 L.239, no ice
- Dec 3 \<50% ice cover
- Dec 4 ~60% ice cover
- Dec 5 100% ice cover; ice on
- Nov 17, 2010 L.239, no ice
- Nov 22 L.239, ice free except for E. Bay frozen
- Nov 23 L.239, ice free except for E. Bay
- Nov 24 100% ice cover; ice-on
- Dec 1, 2015 L.239 very little ice; JN
- Dec 2-6 L.239 ~80% ice cover; JN
- Dec 7 AM L.239 ~80-85%; JN
- Dec 7 PM L.239 ~90%; KS & KB
- Dec 8 AM L.239 ~90%; KS & KB
- Dec 9 AM L.239 ~95%; ice fog and heavily overcast; KB
- Dec 9 PM L.239 ~95%; JN
- This continues until Dec 20
- Dec 20 AM L. 239 100% Ice cover – GF (from low vantage point)
- Dec 25 L 239 first day of 100% ice cover, as verified by daily satellite imagery.

The lengthy freeze of the lake in 2015 was due to abnormally warm weather in late November and early December. New records for maximum air temperature were recorded at many locations in southern Manitoba on December 9<sup>th</sup>, 2015 including Winnipeg at +5.6<sup>o</sup>C.

#### Vantage Points

Vantage points that have been used to view the ice on Lake 239 include:
- The dock on Lake 239
- The meteorological site
- The top of Lake 303 ridge on the road.

A high vantage point is best. It can be quite difficult to estimate cover from a low vantage point, see example above (Dec 20, 2015). Following the forest fire in 1980, the latter two locations offered a good view of the lake, however in recent years the gradual increase in tree height now obscures the view almost entirely.

The view from the cleared helicopter pad near the Lake 239 outflow offers a good view of the lake but it is sometimes necessary to go to the beaches at the NW and NE corners of the lake to be certain. Estimating the ice coverage is easiest when a light snow cover is present, creating a contrast to the dark open water. This was not the case in 2015 because much of the ice was dark and unsafe to venture on.

### Trail cameras and satellite imagery (ICE2)

Similarly to the in-person visual observations, this method uses criteria of 80% of the lake surface ice-covered for ice-on and 80% of the lake surface ice-free conditions for ice-off, and accounts for re-freeze/re-thaw situations by taking the first date for ice on and the last date for ice off (and noting the alternate dates in the comments). The difference is that instead of or in addition to in-person visual observations, trail cameras are used, as well as satellite imagery in some cases.

While in-person visual observations have been consistently undertaken on Lake 239 since 1969, the trail camera method was introduced in 2016. For Lake 239 the trail camera photos provide confirmation of the visual observations. For other lakes, the trail camera photos are the primary means of quantifying the ice-on and ice-off dates. Since the period of ice-formation, ice-decay and snow cover are not binary events (i.e. on/off) but occur over a period of time. The historical photos may be of future use to further characterize conditions.

In general, the orientation of cameras is in part practical, but also is intended to capture as much of the lake as possible or, for larger lakes (e.g. Winnage), a large basin. In some cases, more than one camera is used. For Lake 239, one camera is mounted facing north, at the top of a 10 m tower located at the south end of the lake (the cleared helicopter pad near the Lake 239 outflow). A second camera is typically mounted about 1.5 m above the ground on a tree at the north end of the lake, facing south. The trail camera approach was also used to validate satellite photos of ice coverage for a series of lakes that spanned a lake size gradient (20 – 1000 ha; Higgins et al. 2021).

A combination of Bushnell, Moultrie, and Reconyx brand cameras were deployed on trees along the shorelines of the lakes (similarly to the Lake 239 camera positions described above). Cameras typically collect hourly photos. For larger lakes where the camera field of view included only a small proportion of lake area (i.e., an embayment), the photos were used to ground truth satellite imagery, which was then used to estimate the ice-on or ice-off date of the lake.

## References

Higgins, S., Desjardins, C. M., Drouin, H., Hrenchuk, L. E., & Van Der Sanden, J. J. (2021). The Role of Climate and Lake Size in Regulating the Ice Phenology of Boreal Lakes. *Journal of Geophysical Research*, *126*(3), nan. [https://doi.org/https://doi.org/10.1029/2020jg005898](https://doi.org/https:/doi.org/10.1029/2020jg005898)

IISD Experimental Lakes Area. (2023). IISD Experimental Lakes Area: Bathymetry Data Package, 1968-2023 ver 4. Environmental Data Initiative. <https://doi.org/10.6073/pasta/97063072cc506710c03c3362ff92bdcb> (Accessed 2024-08-19).

Lake of the Woods News, Vol. 30, No. 1, March 2000, p.19

Sharma, S., Filazzola, A., Nguyen, T., Imrit, M. A., Blagrave, K., Bouffard, D., Daly, J., Feldman, H., Feldsine, N., Hendricks-Franssen, H., Granin, N., Hecock, R., L’Abée-Lund, J. H., Hopkins, E., Howk, N., Iacono, M., Knoll, L. B., Korhonen, J., Malmquist, H. J., . . . Magnuson, J. J. (2022). Long-term ice phenology records spanning up to 578 years for 78 lakes around the Northern Hemisphere. *Scientific Data*, *9*(1). https://doi.org/10.1038/s41597-022-01391-6
