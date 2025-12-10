# Zooplankton Data – Information Sheet

Authors: IISD Experimental Lakes Area, Michael Paterson, Patrique Bulloch, Chris Hay  

## Contents
- [General Information](#general-information)
  * [Background of the dataset](#background-of-the-dataset)
  * [Considerations when using the data](#considerations-when-using-the-data)
- [Methods](#methods)
  * [Sampling](#sampling)
    + [Sampling Methods Summary Table](#sampling-methods-summary-table)
    + [Instrumentation](#instrumentation)
    + [Sample preservation](#sample-preservation)
  * [Analysis](#analysis)
    + [Zooplankton identification](#zooplankton-identification)
  * [Processing Data](#processing-data)
    + [Calculated parameters](#calculated-parameters)
    + [Biomass estimation](#biomass-estimation)
    + [QA/QC checks and method comparisons](#qa-qc-checks-and-method-comparisons)
- [Data Dictionary](#data-dictionary)
  * [List of columns by table](#list-of-columns-by-table)
  * [Column Definitions](#column-definitions)
  * [Domains](#domains)
- [References](#references)

# General Information

## Background of the dataset

*Zooplankton data have been collected from various lakes at the IISD Experimental Lakes Area (ELA), in Northwestern Ontario Canada since 1969. The collection of zooplankton samples was undertaken as part of ELA’s Long-term Ecological Research (LTER) program and as supporting data for various projects at the ELA. The methodology of sampling changed several times from 1969-1979 and differs among lakes. The two most commonly used sampling methods in current use (zoonets and Salki tubes) were adopted for their respective suite of lakes in 1979 and 1988 respectively.*

*Zooplankton taxonomy and counts have been performed by various individuals, though considerable efforts have been made to minimize the number of different analysts to reduce variability in the long-term record. Changes in taxonomic nomenclature and zooplankton identification protocols have been tracked and, where necessary, taxonomy has been harmonized. The original designations used by different taxonomists are also available. The datasets are being transferred from the Microsoft Access database to the Postgres master database.*

## Considerations when using the data

- Different methods have been used for collecting zooplankton in different lakes and at different times and they do not always provide comparable estimates of abundance (column entitled “method”). Samples collected using the Schindler-Patalas trap and various nets were collected at center-buoy only and comparisons suggest they provide similar results when integrated through the water column (Johannsson et al. 1992). Samples collected with the Salki-Patalas tubes were collected at multiple stations and the data are not directly relatable with data collected using the other methods at center-buoy.

- Different counting protocols have also been used over the years. Most importantly, there are variations in the way juvenile copepods have been counted. Prior to 1998/99, juvenile copepods were only identified to group (calanoids, cyclopoids) and as early and later stages (c1-c3, c4-c5). After 1998/99, counters were asked to identify c4-c5 stages to species, if possible. As a result, counts of c4-c5 copepods IDed only to group typically drop to zero after 1998/99 and species- level counts of c4-c5 copepods show up in the data set. If you want comparable data through the entire period of record, it is necessary to combine all c4-5 species-level data obtained post 1998/99 at the group level. Adult copepods have been identified to species and sex in all samples.

- There have been changes in counters over the years. Occasionally, different counters may use different names for the same taxon. I have provided data where names have been harmonized as best as is possible. For some taxa, this has meant lumping at higher taxonomic levels (e.g., genus).

- Not all counters identified rotifers (column entitled “Rotifers”; if code = “yes”, they were counted).

- The data are all in numbers/L.

- Some samples were collected through the ice. Since this was not done in all years, winter samples should be dropped to obtain comparable annual averages (if that is a goal). Counts are typically very low in winter and skew the data if they aren’t removed. Under-ice samples have all been collected using a net at center-buoy. For lakes sampled with a tube in the ice-free season, under-ice samples collected at center-buoy with a net are not directly comparable for abundance estimates.

# Methods

## Sampling 

### Sampling Methods Summary Table

The table below summarizes the main methods used throughout ELA’s history.

| Lakes | Years | Device | Remarks | References |
| --- | --- | --- | --- | --- |    
| 223, 224, 226, 227, 239, 304 | 1969-1975 | 28.7 L Schindler-Patalas trap; different size meshes were used | Vertical series at Center-buoy (CB) – samples were combined into composites for the epilimnion, metalimnion, and hypolimnion based on temperature profiles | Chang & Malley 1987; Schindler & Noven 1971 |
| 226 | 1975-1976 | 2m long, transparent acrylic tube | Epilimnion only | Chang & Malley 1987 |
| 223, 224, 226, 227 | 1977 | 4-barrel non-closing net; 2 mesh sizes were used: small = 53 um, large = 153 um | Vertical hauls from various depths to surface at CB; usually 3 hauls | Chang & Malley 1987 |
| 223, 226, 227 | 1978 | 2-barrel closing sampler, 13 cm each mouth diameter; 2 nets were used: small = 53 um; large = 153 um | 3 hauls X depth of sampling layer at CB | Chang & Malley 1987 |
| All lakes after 1979 except those listed below for tubes | 1979-present | 2-barrel closing sampler; 53 um; 13 cm each mouth diameter | 2 hauls X depth of sampling layer at CB | Chang & Malley 1987 |
| Variability Lakes 114, 149, 164, 165, 191, 226, 260, 303, 304, 373, 377, 378, 442, 632, 658, 938, 979 FLUDEX Reservoirs | 1988-present | Flexible PVC hose (7.6 cm mouth diameter) through 72 um net<br>After 1998 – 53 um net | One haul per station at 5-7 stations located around each lake | Salki (1993, 1995) |

### Instrumentation

**Schindler-Patalas traps**

In the earliest years at ELA, a 28.7L Schindler-Patalas trap was used to collect zooplankton (Schindler 1969). Different mesh sizes were used in different lakes and years. Typically, samples were collected at 1m or 2m intervals and then combined into composites for the epilimnion, metalimnion, and hypolimnion as defined by temperature and light. The epilimnion extended from the surface to the depth where temperature changes exceeded 1C/m. The metalimnion extended from the base of the epilimnion to the depth of 1% light penetration. After turnover, samples from all depths were pooled. In the database, there are scripts to generate whole-water column averages based on data from the separate strata.

**2m long, transparent acrylic tube**

In 1975 and 1976, zooplankton samples were collected using a 9.1L plexiglass tube 7.6 cm in diameter and 2m in length. 10 samples were collected from the upper 2m of the water column, sieved with a 53 µm mesh, and combined into a single sample for counting. Because these samples are fundamentally different from water column samples collected in other years, they have not been used in annual estimates generated from the database.

**4-barrel, non-closing net**

In 1977, a 4-barrel net was used that consisted of 2 pairs of 30 cm long plexiglass tubes held at right angles to each other with a steel frame. Two of the tubes were large (15cm ID) with a 150 µm mesh and 2 were smaller (7.5cm ID) with a 53µm mesh. All nets were 1.5m long with a 3.5cm bucket. The nets were hauled from 3 layers: 1) from the lake bottom to the lake surface; 2) from the base of the metalimnion to the lake surface; and 3) from the base of the epilimnion to the lake surface. Three replicates were collected from each layer and layers were defined by temperature as described above for Schindler-Patalas traps. Densities in the different strata were calculated by subtraction and negative densities were assumed to be zero. Only data from the small net are stored in the database.

**2-barrel, 1 net, closing**

In 1978, a 2-barrel net was used that consisted of 2 plexiglass tubes (12.9cm ID) mounted 22 cm apart on a metal frame (see Fig 1 in Chang et al. 1980). Each barrel had a lid that could be closed with a messenger. One cylinder had a 53 µm net and the other had a 150 µm net. Both nets were 1.5m long with a collecting bucket. The nets were hauled through the stratum of interest and closed with the messenger. Only data from the 53µm net are stored in the database.

**2-barrel, 2 net, closing**

Since 1998, many lakes have been sampled using a 2-barrel closing net as described by Chang et al. (1980). This net is the same as the 2-barrel closing net described above except that both nets are 53µm. Each net is built with a 12.7 cm diameter hoop affixed to a rope marked in 0.5 m increments to control the sampling depth – ropes are periodically re-marked or replaced due to stretching. For consistency, a pair of nets (labelled for example, 2024-L442-1 and 2024-L442-2) is assigned to each lake for a period of two years before being replaced. The net itself is a 1.5m long 53 µm mesh cone that terminates into a spigot equipped with a ball valve. The spigot is installed by cutting a hole at the bottom of the mesh cone, roughly the same size as the spigot diameter. The spigot is secured into place with a hose clamp and electrical tape. The end of the spigot that contacts the net is coated in liquid electrical tape to blunt any edges that may create tears in the mesh. Out of the water, the nets drain into the bottom of the net. The net is rinsed and drained into a 1L bottle to collect the trapped zooplankton. In some years, the nets were hauled through the stratum of interest and closed with the messenger; in recent years, the lids have been removed and the entire water column has been sampled.

Here is a photo showing the contents of a zooplankton haul collected with the double-barrel net being drained into a sampling container.

<img src="attachments\image1.jpeg" style="width:3.34375in;height:5in" alt="Two people on a boat on a lake. The contents of a zooplankton haul collected with the double-barrel net is being drained into a sampling container." />  
<br/><br/><!--these html brs is just for an extra line break after the image-->

**Single barrel net**

To accommodate sampling through the ice and a hole created with an ice-auger, a net, using one barrel of the 2-barrel, 2-net closing net, has been used in winter.

**Wisconsin nets**

On occasion, single and double Wisconsin nets have been used to sample ELA lakes. Mesh sizes and mouth openings have varied among samples. Typically, the net was towed from just above the lake bottom to the surface.

**Salki-Patalas tubes**

Salki-Patalas tubes are lengths of flexible 7.6 cm diameter PVC tubes with a distal plexiglass pipe with an external lead weight to which a retriever cord is attached (Salki 1993). Tubes are long enough to match the deepest point of their assigned lake. One tube is assigned to each lake and is stored at its lake in a bin. A rope marked with 0.5 m increments is affixed to the weighted distal end of the tube, to control the sampling depth, which is 0.25m above the lake bottom. Tubes are emptied into a 1L bottle by funneling into a 53 µm mesh net to retain zooplankton, equipped with a spigot and ball valve. Prior to 1998, a 72 µm net was used. For ease of handling, the net is placed in a custom-made holder (a wooden plank with a hole large enough to fit the filtering net) that is secured to the boat with a clamp.

A major difference between lakes sampled with the Salki-Patalas tubes and other methods is that tube lakes are sampled at multiple stations. Zooplankton stations are marked using floats secured at different known depths. Stations have been distributed around each lake to approximate the contribution of different depths to overall lake bathymetry. Each float consists of a buoy equipped with a ring screw to allow mooring and is anchored to the lake bottom with a cinder block or other heavy object (Campbell & Salki 1992). These are used to ensure consistency in spatial sampling, while providing the added benefit of a secure anchorage to minimize boat drift. Depths are always verified with a hand-held depth sounder to account for changes in water level. Variations in the volume of tube samples are recorded and directly entered in the database.

In some years, tube lakes were sampled at different fixed depths in the water column. To differentiate these fixed depths from depths defined by temperature using nets and Schindler-Patalas traps (see above), they are denoted as upper, middle or deep samples in the database. Different depths were sampled by placing the hose mouth in the net and retrieving the tail end the required meters and then switching to another net for the next sampling layers (Salki 1993). In some years, separate samples were also collected from the littoral zone, which was defined as depths less than 3m.

**Inflow and outflow sample container**

In some years, inflows and outflows to ELA lakes were sampled for zooplankton. A 2L container was used to collect 50L of water, which was then filtered through a zooplankton net.

### Sample preservation 

Prior to 1998, samples were preserved in 5% formalin in the laboratory as soon after collection as possible. After 1998, samples were narcotized with methanol in the field (Gannon and Gannon 1975) and then preserved with 5% sugar-formalin in the laboratory (Prepas 1978). In recent decades, samples were washed into 1L polyethylene bottles containing 25 mL of methanol. Prior to shipping for taxonomic and abundance analyses, samples were filtered down to a final volume of 40 mL, if possible, and stored in glass vials.

Sampled depth and net or tube diameters were used to estimate the volume of lake water sieved by the net or tube assuming a net efficiency of 100%. This information along with other metadata such as weather conditions are entered into notebooks or, in recent years, a digital database using Esri’s Survey123 application.

## Analysis

### Zooplankton identification

Over the years, several different zooplankton taxonomists have enumerated samples from ELA and several different counting and identification protocols have been used. In general, zooplankton were identified and enumerated from subsamples that varied in size from 1/80 to all of the original sample, depending on the relative abundance of the group. The entire sample volume is examined for large crustaceans and for insects. A minimum of 200-300 microcrustacea, excluding juvenile stages, are identified to species and sex.

Some important variations in counting protocols include:

- Not all taxonomists identified and counted rotifers. In the database, samples including rotifer counts are noted with a “yes” in the column entitled “rotifers”.

- Several different approaches have been used to identify copepodid stages:

  - Prior to 1998/99, juvenile copepods counted by all taxonomists, except AGS (Alex Salki), were only identified to group (calanoids, cyclopoids) and as early and later stages (c1-c3, c4-c5). Occasionally, copepodid stages were IDed to individual stage. In water column estimates determined from the database, I have combined these into c1-c3 and c4-c5 groupings to match other identifications.

  - After 1998/99, all counters (except AGS) identified c4-c5 stages to species, if possible. C1-3 stages were still identified only to group.

  - AGS identified copepodid stages to c1-c5 by species in all years that he counted.

  - These variations in counting protocols have important implications for data interpretation. Counts of undifferentiated c4-c5 copepods IDed only to group typically drop to zero after 1998/99 and species- level counts of c4-c5 copepods begin to show up in the data set. To obtain comparable data through the entire period of record, it is necessary to: either (this sentence requires review) "combine all the c4-5 species-level data obtained post 1998/99 at the group level" or "throw out all the c4-5 species-level data obtained post 1998/99 and combine c4-c5 counts at the group level".

  - Adult copepods have been identified to species and sex in all samples.

- Free eggs and eggs attached to adult females were counted by all counters, except AGS. AGS separately counted ovigerous and non-ovigerous females.

- Occasionally, different counters may have used different names for the same taxon. Data are available where names are provided in 2 different ways. First, data can be provided using the original taxonomic names provided by the counter, except for updates in taxonomic nomenclature (see below). Secondly, I have attempted to harmonize the taxonomies as best as is possible. For some taxa, this has meant lumping counts at higher taxonomic levels (e.g., genus). I have also lumped taxa that are especially problematic to identify and where I have low confidence in the identifications (e.g., Chydorid cladocerans, bosminids, and some *Daphnia* groups). The way taxa have been lumped is described in the file “taxon_codes_all_common-taxonomy”

- Over the 56+ year history of ELA, the taxonomy of several zooplankton species has been updated (e.g., *Holopedium*, *Mysis*, *Diaphanosoma*, *Tropocyclops*). I have harmonized these names throughout the dataset.

- The primary data in the database are densities/L. If the original counts from subsamples are needed, the following caveats apply:

  - AGS counted samples using a voice system that did not store the original counts electronically. Data counted by AGS are entered in the database as densities per L and can be identified when the zooplankton count per sample equals the density estimate (split multiplier = 1). Original counts for most of these samples are available in the original count sheets but have not been entered electronically.

  - Counts prior to 1996 were entered electronically as counts per mL of subsample. Hence, these are not the original counts, which are available on the original hand-written data sheets. Exceptions to this are data entered for Lakes 224, 240, 302N, and 375 for samples collected prior to 1996.

## Processing Data

### Calculated parameters

Metadata previously entered into field notebooks or the Survey123 application are used to calculate sampled volumes of lake water by using this equation:  
$\left[ \pi * r^{2} \right] * d * n$<!--This is LaTeX code so the equation displays nicely in GitHub Markdown-->  
where $r$ is the radius of the net or tube, $d$ is the depth of the sample, and $n$ is the number of hauls.  

Count data and sample volumes are then used to calculate abundance per litre (estimate of total abundance in the sample/ volume of water sieved in the sample).

### Biomass estimation

Biomass was estimated by multiplying the taxon densities (numbers per liter) by an estimate of the mass per individual for each taxon.  All estimates of the mass per individual of different taxa and life stages in samples collected from different lakes and dates were determined from length-weight regressions, but the resolution varies considerably among samples. In some lakes and years, zooplankton in each sample were measured and these values are used.  In other lakes and years, measures were completed on composite samples made up from subsamples from each sampling date in each year and represent an annual average length for each taxon. In this case, the annual estimates were used for all dates sampled in that lake in that year.  Finally, if no measures were done in a lake and year, an average derived using all existing data from that lake (if data exist) or for all lakes at ELA was used.  All lengths were converted to masses using length-weight regressions in Malley et al. (1989), Lawrence et al. (1987), Allen et al. (1994), McCauley (1984), Schindler and Noven (1971), and Paterson (unpublished).  If regressions existed for a particular ELA lake, these were used preferentially for that lake.  
For group biomass estimates, I used the protocols of Dodson (1992) and removed taxa that were littoral (Chydorids except Chydorus, Macrothricids, etc.)  

### QA/QC checks and method comparisons

to do or separate document

# Data Dictionary

## List of tables and views
There are datasets, each corresponding with one table and one view. These are best summarized with this overview table, based on a few key criteria: level, meta/data type, and taxonomy. From top to bottom roughly corresponds with less to more processed data. Which dataset you use will depend on your needs. For example, do you just want a list of samples and when they were collected,  species-level data for each sample (harmonized into a common taxonomy over time periods/ analyst taonomists), or do you want biomass data summarized into a handful of taxonomic groups?

| Dataset Code | Dataset Name                                                    | Table Name                   | View Name | Level                | Meta/data table type         | Taxonomy type                            |
| ------------ | --------------------------------------------------------------- | ---------------------------- | --------- | -------------------- | ---------------------------- | ---------------------------------------- |
| Z01          | Zooplankton raw samples metadata                             | bio_zoop_raw_sampling        | …_view    | Raw                  | Metadata on samples          | N/A                                      |
| Z02          | Zooplankton raw density data                                 | bio_zoop_raw_density         | …_view    | Raw                  | Data - Abundance             | Raw                                      |
| Z03          | Zooplankton processed data -<br>samples metadata                | bio_zoop_proc_sampling       | …_view    | Processed (taxa/spp) | Metadata on samples          | N/A                                      |
| Z04          | Zooplankton processed data -<br>abundance and biomass for the<br>original taxonomy | bio_zoop_proc_abd_biom_og    | …_view    | Processed (taxa/spp) | Data - Abundance and Biomass | Original                                 |
| Z05          | Zooplankton processed data -<br>abundance and biomass for the<br>common (harmonized) taxonomy | bio_zoop_proc_abd_biom_comm  | …_view    | Processed (taxa/spp) | Data - Abundance and Biomass | Common                                   |
| Z06          | Zooplankton processed data -<br>abundance and biomass at the<br>group level (higher<br>taxonomic level summary) | bio_zoop_proc_biomass_groups | …_view    | Processed (groups)   | Data - Biomass               | Groups (raw vs og vs comm is irrelevant) |


## List of columns by view
The tables below are actually "views" in terms of database terminology. Tables follow rules of normalization, which means they are typically difficult to use for data analysis without first joining together data with metadata, i.e, creating these views. Hence in this case, unlike other info sheets, we do not mark with an asterisk the "keys" between tables (columns on which to join), since joining has already been done. Instead we indicate with a "+" symbol the columns that have been joined-in from other tables (or otherwise were produced). Those columns effectively provide important metadata to better use and understand each of these views.

**bio_zoop_raw_sampling_view**
- record_key
- dataset_code
- dataset_name +
- sample_key_raw
- sample_type
- zone
- monitoring_location_name
- region_id
- year +
- sample_date
- sample_time
- strata_layer_name
- collector_id
- start_depth
- end_depth
- end_depth_2
- gear_type_code
- gear_type_desc +
- mouth_diameter
- mesh_size
- num_hauls
- strata_volume
- sample_override
- vial_id
- box_number
- vial_notes
- sample_volume
- sample_notes
- account
- update_date
- version

**bio_zoop_raw_density_view**
- record_key
- dataset_code
- dataset_name +
- sample_key_raw
- zone +
- monitoring_location_name +
- region_id +
- year +
- sample_date +
- sample_time +
- strata_layer_name +
- start_depth +
- end_depth +
- end_depth_2 +
- gear_type_code +
- gear_type_desc +
- mesh_size +
- sample_type +
- initial_volume
- strata_volume +
- vial_id +
- box_number +
- vial_notes +
- sample_volume +
- count_sample
- sub_sample_vol
- analyst
- observations
- rotifers
- taxon_code_raw
- species_name +
- life_stage_code
- lifestage_name +
- sex_code
- sex +
- split_multiplier
- zoo_sample_count
- total_number
- num_l_raw
- account
- update_date
- version

**bio_zoop_proc_sampling_view**
- record_key
- dataset_code
- dataset_name +
- sample_key_proc
- sample_type
- zone
- monitoring_location_name
- region_id
- year +
- sample_date
- sample_time
- gear_type_code
- gear_type_desc +
- mesh_size
- account
- update_date
- version

**bio_zoop_proc_abd_biom_og_view**
- record_key
- dataset_code
- dataset_name +
- sample_key_proc
- zone +
- monitoring_location_name +
- region_id +
- year +
- sample_date +
- sample_time +
- sample_type +
- gear_type_code +
- gear_type_desc +
- mesh_size +
- rotifers
- taxon_code_proc
- num_l
- tmp_group
- tmp_taxon_name
- tmp_graph_name
- day_size
- ug_ind_day
- year_size
- ug_ind_year
- sum
- default_
- ug_ind_default
- ug_l_day
- ug_l_year
- ug_l_default
- day_count
- year_count
- default_count
- ug_l
- account
- update_date
- version

**bio_zoop_proc_abd_biom_comm_view**
- record_key
- dataset_code
- dataset_name +
- sample_key_proc
- zone +
- monitoring_location_name +
- region_id +
- year +
- sample_date +
- sample_time +
- sample_type +
- gear_type_code +
- gear_type_desc +
- mesh_size +
- rotifers
- taxon_code_proc
- num_l_proc
- tmp_group
- tmp_taxon_name
- tmp_graph_name
- ug_ind
- ug_l
- account
- update_date
- version

**bio_zoop_proc_biomass_groups_view**
- record_key
- dataset_code
- dataset_name +
- sample_key_proc
- zone +
- monitoring_location_name +
- region_id +
- year +
- sample_date +
- sample_time +
- sample_type +
- gear_type_code +
- gear_type_desc +
- biom_grp_calanoid
- biom_grp_cladocera
- biom_grp_cyclopoid
- biom_grp_rotifer
- biom_total_copepods
- account
- update_date
- version


## Column Definitions

In progress...

# References

Allen, G., N. D. Yan, and W. T. Geiling. 1994. ZEBRA2 - Zooplankton enumeration and biomass routines for APIOS: A semi-automated sample processing system for zooplankton ecologists. PIBS 2872.

Campbell, P., and A. G. Salki. 1992. A durable all-season marker float and mooring buoy for limnological field studies. Canadian Technical Report of Fisheries and Aquatic Sciences 1852.

Chang, P. S. S., and D. F. Malley. 1987. Zooplankton in Lake 223, Experimental Lakes Area, northwestern Ontario, 1974-1983. Canadian Data Report of Fisheries and Aquatic Sciences 665.

Chang, P. S. S., D. F. Malley, W. J. Findlay, G. Mueller, and R. T. Barnes. 1980. Species composition and seasonal abundance of zooplankton in Lake 227, Experimental Lakes Area, northwestern Ontario, 1969-1978. Canadian Data Report of Fisheries and Aquatic Sciences 182.

Dodson, S. 1992. Predicting crustacean zooplankton species richness. Limnology and Oceanography 37: 848-856.	

Gannon, J. E., and S. A. Gannon. 1975. Notes on the narcotization of crustacean zooplankton. Crustaceana 28:220-224.

Johannsson, O. E., M. A. Shaw, N. D. Yan, J.-M. Filion, and D. F. Malley. 1992. A comparison of freshwater zooplankton sampling gear: Nets, traps, and submersible pump. Canadian Technical Report of Fisheries and Aquatic Sciences 1894.

Lawrence, S. G., Df. Malley, W.J. Findlay, M.A. MacIver, and I.L. Delbaere. 1987. Method for estimating dry weight of freshwater planktonic crustaceans from measures of length and shape. Canadian Journal of Fisheries and Aquatic Sciences 44  (Suppl.  1): 264-274.	

Malley, D. F., S. G. Lawrence, M. A. MacIver, and W. J. Findlay. 1989. Range of variation in estimates of dry weight for planktonic Crustacea and Rotifera from temperate North American lakes. Canadian Technical Report of Fisheries and Aquatic Sciences 1666.

McCauley, E. 1984. The estimation of the abundance and biomass of zooplankton in samples. A Manual on Methods for the Assessment of Secondary Productivity in Fresh Waters. J. A. Downing and F. H. Rigler. Oxford, Blackwell Scientific Publishers: 228-265.	

Prepas, E. 1978. Sugar-frosted *Daphnia*: an improved fixation technique for Cladocera. Limnology and Oceanography **23**:557-559.

Salki, A. G. 1993. Lake variation and climate change study: VII. Crustacean plankton of a lake flushing rate series in the Experimental Lakes Area, northwestern Ontario, 1987-1990. Canadian Data Report of Fisheries and Aquatic Sciences 880.

Salki, A. 1995. Lake variation and climate change study: crustacean plankton of a lake flushing rate series in the Experimental Lakes Area, northwestern Ontario, 1991-1993, and lakes Nipigon and Superior, 1991. Canadian Data Report of Fisheries and Aquatic Sciences 967, Winnipeg.

Schindler, D. W. 1969. Two useful devices for vertical plankton and water sampling. Journal of the Fisheries Research Board of Canada **26**:1948-1955.

Schindler, D. W., and B. Noven. 1971. Vertical distribution and seasonal abundance of zooplankton in two shallow lakes of the Experimental Lakes Area, northwestern Ontario. Journal of the Fisheries Research Board of Canada **28**:245-256.
