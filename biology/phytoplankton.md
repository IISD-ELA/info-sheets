# Phytoplankton Data – Information Sheet

**Authors**: IISD Experimental Lakes Area, Scott Higgins

**Last Updated**: July 19, 2024

**Migrated By**: Delvin So

- [Phytoplankton Data – Information Sheet](#phytoplankton-data--information-sheet)
    - [General Background](#general-background)
    - [Methods](#methods)
        - [Sampling](#sampling)
        - [Analysis](#analysis)
        - [Processing](#processing)
    - [Data Dictionary](#data-dictionary)
        - [List of columns by table](#list-of-columns-by-table)
        - [Column Definitions](#column-definitions)
    - [References](#references)


## General Background

Phytoplankton data have been collected from various lakes at the IISD
Experimental Lakes Area (ELA), in Northwestern Ontario Canada since
1969. The collection of phytoplankton samples was undertaken as part of
ELA’s Long-term Ecological Research (LTER) program.

## Methods

### Sampling

Integrated water samples were collected from the epilimnion and
metalimnion (when present) of LTER lakes approximately biweekly during
the open water season (c. May through October). The epilimnion was
defined as the upper surface layer, which extended from the air-water
interface to the thermocline. The metalimnion was operationally defined
as extending from the thermocline to the bottom of the euphotic zone (1%
surface irradiance). The samples were collected in opaque and insulated
sampling bottles as described by Shearer (1978). Subsamples (c. 125 mL)
were taken and preserved with Lugol’s solution and stored in the dark at
room temperature until analysis.

A 2 mL aliquot was gravity settled for 24 hours and species
identification and enumeration were undertaken at 125X and 550X using
the Utermol method (Nauwerek 1963). Cell measurements were undertaken on
each species to maximum of 50 individuals, and cell numbers were then
converted to wet weight biomass by estimating cell volumes of each
species by fitting cell shapes to geometric formulae and assuming a
specific gravity of 1.0 (Vollenweider 1968).

### Processing

Sample data were stored in their raw form within the 'Tabular Data -
Phytoplankton Species Abundance, Biomass and Cell Volume' table. The
summarized abundance and biomass within each sample were calculated for
7 taxonomic groups by summing values within each taxonomic grouping. The
first number within each species code represents the taxonomic group (1=
cyanophyte, 2= chlorophyte, 3= euglenophyte, 4= chrysophyte, 5= diatom,
6= cryptophyte, 7= dinoflagellate). Total abundance and total biomass
values provided in the 'Tabular Data - Phytoplankton Group Biomass and
Total Biomass' table were calculated by summing values across all
taxonomic groups for each sample.

## Data Dictionary

### List of columns by table

Keys are indicated with asterisks (here they are compound keys with more
than one field)

Metadata - Lake\_information

- monitoring\_location\_name\*
- area\_catchment
- area\_surface
- depth\_mean
- depth\_max
- volume\_total
- order\_lake
- mixing\_status
- latitude
- longitude

Tabular Data - Phytoplankton Group Biomass and Total Biomass

- monitoring\_location\_name \*
- date\_collected\*
- stratum\*
- depth\_upper
- depth\_lower
- cyanobacteria
- chlorophyte
- euglenophyte
- chrysophyte
- diatoms
- cryptophyte
- dinoflagellate
- biomass\_total

Tabular Data - Phytoplankton Species Abundance, Biomass and Cell Volume

- monitoring\_location\_name \*

- date\_collected \*

- stratum\*

- depth\_upper

- depth\_lower

- species\_code\*

- volume\_cell

- density

- biomass

Phytoplankton Species Codes and Taxonomy

- species\_code\*

- group

- phylum

- class

- order

- family

- genus

- specific\_epithet

- variety

- species

Phytoplankton Species Trophic Type

- species\_code\*

- trophic\_type

### Column Definitions



<table>
<colgroup>
<col style="width: 18%" />
<col style="width: 13%" />
<col style="width: 12%" />
<col style="width: 55%" />
</colgroup>
<thead>
<tr>
<th><strong>column name (alphabetical)</strong></th>
<th><strong>data type</strong></th>
<th><strong>unit</strong></th>
<th><strong>definition</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td>area_catchment</td>
<td>numerical</td>
<td>kilometers squared</td>
<td>Area of the terrestrial catchment associated with the specified
monitoring_location_name. This is the watershed area, not including the
lake itself.</td>
</tr>
<tr>
<td>area_surface</td>
<td>numerical</td>
<td>meters squared</td>
<td>The surface area of the lake associated with the specified
monitoring_location_name. The area excludes islands and protruding
boulders (where survey methods differentiated). Values are calculated to
0.01 metres squared, but the error would be greater than 1 (in most
cases the DEM used to calculate the area has 1 metre resolution). The
area is calculated from a geospatial polygon produced from a combination
of satellite imagery tracing and transects on the lake.</td>
</tr>
<tr>
<td>biomass</td>
<td>numerical</td>
<td>milligrams per meter cubed</td>
<td>Phytoplankton biomass concentration for the specified taxon
(estimate; wet weight).</td>
</tr>
<tr>
<td><p>chlorophyte_</p>
<p>biomass</p></td>
<td>numerical</td>
<td>milligram per meter cubed</td>
<td>Biomass of phytoplankton group.</td>
</tr>
<tr>
<td><p>chrysophyte_</p>
<p>biomass</p></td>
<td>numerical</td>
<td>milligram per meter cubed</td>
<td>Biomass of phytoplankton group.</td>
</tr>
<tr>
<td>class</td>
<td>text</td>
<td>n/a</td>
<td>taxonomic unit</td>
</tr>
<tr>
<td><p>cryptophyte_</p>
<p>biomass</p></td>
<td>numerical</td>
<td>milligram per meter cubed</td>
<td>Biomass of phytoplankton group.</td>
</tr>
<tr>
<td><p>cyanobacteria_</p>
<p>biomass</p></td>
<td>numerical</td>
<td>milligram per meter cubed</td>
<td>Biomass of phytoplankton group.</td>
</tr>
<tr>
<td>date_collected</td>
<td>date</td>
<td>n/a</td>
<td>Sample collection date.</td>
</tr>
<tr>
<td>density</td>
<td>numerical</td>
<td>number per meter cubed</td>
<td>Density of individuals present from the taxon (abundance over
volume).</td>
</tr>
<tr>
<td>depth_lower</td>
<td>numerical</td>
<td>meters</td>
<td>The lower depth level in consideration of the depth range for the
characteristic and value in question. For example, in a depth range of
2.5 to 5.0 metres deep, the lower depth is 5.0.</td>
</tr>
<tr>
<td>depth_max</td>
<td>numerical</td>
<td>meters</td>
<td>The maximum depth of the lake associated with the specified
monitoring_locaiton_name. That is, the depth at the deepest point on the
day of survey. The value is calculated from a GIS raster DEM, produced
using sonar data from transects across the lake and using satellite
imagery to trace its extent. Values are calculated to 0.01 metres,
corresponding in most cases with raw sonar readings provided to 0.01
metres, but the degree of error would be greater.</td>
</tr>
<tr>
<td>depth_mean</td>
<td>numerical</td>
<td>meters</td>
<td>The mean (average) depth of the lake associated with the specified
monitoring_location_name. The value is calculated from a GIS raster DEM,
so is based on the depth values across the entire lake. The DEM was
produced using sonar data from transects across the lake, and using
satellite imagery to trace its extent. Values are calculated to 0.01
metres, corresponding in most cases with raw sonar readings provided to
0.01 metres, but the degree of error would be greater.</td>
</tr>
<tr>
<td>depth_upper</td>
<td>numerical</td>
<td>meters</td>
<td>The upper depth level in consideration of the depth range for the
characteristic and value in question. For example, in a depth range of
2.5 to 5.0 metres deep, the upper depth is 2.5.</td>
</tr>
<tr>
<td><p>diatoms_</p>
<p>biomass</p></td>
<td>numerical</td>
<td>milligram per meter cubed</td>
<td>Biomass of phytoplankton group.</td>
</tr>
<tr>
<td><p>dinoflagellate_</p>
<p>biomass</p></td>
<td>numerical</td>
<td>milligram per meter cubed</td>
<td>Biomass of phytoplankton group.</td>
</tr>
<tr>
<td><p>euglenophyte_</p>
<p>biomass</p></td>
<td>numerical</td>
<td>milligram per meter cubed</td>
<td>Biomass of phytoplankton group.</td>
</tr>
<tr>
<td>family</td>
<td>text</td>
<td>n/a</td>
<td>taxonomic unit</td>
</tr>
<tr>
<td>genus</td>
<td>text</td>
<td>n/a</td>
<td>taxonomic unit</td>
</tr>
<tr>
<td>group</td>
<td>categorical</td>
<td>n/a</td>
<td>A non-monophylogenetic group used for practical purposes in
phytoplankton research, around division and phylum level of taxonomic
resolution.</td>
</tr>
<tr>
<td>latitude</td>
<td>numerical</td>
<td>decimal degrees</td>
<td>Latitude part of the coordinates of the specified location. In the
context of the lake metadata table, it is the latitude of the lake's
centre buoy location, determined using handheld GPS.</td>
</tr>
<tr>
<td>longitude</td>
<td>numerical</td>
<td>decimal degrees</td>
<td>Longitude part of the coordinates of the specified location. In the
context of the lake metadata table, it is the longitude of the lake's
centre buoy location, determined using handheld GPS.</td>
</tr>
<tr>
<td>mixing_status</td>
<td>categorical</td>
<td>n/a</td>
<td>Lakes at the ELA research facility are usually defined as ‘dimictic’
or ‘polymictic’. The vertical water column of dimictic lakes mix
partially or completely twice each year (typically in spring after
ice-out and in late autumn prior to complete ice formation).</td>
</tr>
<tr>
<td><p>monitoring_</p>
<p>location_name</p></td>
<td>text</td>
<td>n/a</td>
<td>Name of sampled or surveyed geographic location at the IISD
Experimental Lakes Area field site. The name consists of:
&lt;location&gt; or &lt;location sublocation&gt; or &lt;location
sublocation station&gt;. Location is typically the lake number (each
lake is named with a number, representing the lake's geographical
watershed), sublocation typically specifies LA for "lake" (or a basin,
e.g. NB - north basin, or other), and station is usually CB ("centre
buoy" - at about the deepest point of the lake). Some names do not have
all three parts since a broader area is in question (e.g. for
bathymetry, the entire lake, not just the centre buoy).</td>
</tr>
<tr>
<td>order</td>
<td>text</td>
<td>n/a</td>
<td>taxonomic unit</td>
</tr>
<tr>
<td>order_lake</td>
<td>categorical</td>
<td>n/a</td>
<td>The position of the lake within the drainage network. First order
lakes (lake_order=1) are headwater lakes, second order lakes
(lake_order= 2) receive surface water inflows from 1 upstream lake,
etc.</td>
</tr>
<tr>
<td>phylum</td>
<td>text</td>
<td>n/a</td>
<td>taxonomic unit</td>
</tr>
<tr>
<td>species</td>
<td>text</td>
<td>n/a</td>
<td>taxonomic unit</td>
</tr>
<tr>
<td>species_code</td>
<td>text</td>
<td>n/a</td>
<td>Each species is assigned a code. To link the species code with the
species name and obtain additional taxonomic hierarchy data, join with
the species code table.</td>
</tr>
<tr>
<td>specific_epithet</td>
<td>text</td>
<td>n/a</td>
<td>taxonomic unit</td>
</tr>
<tr>
<td>stratum</td>
<td>categorical</td>
<td>n/a</td>
<td>The lake's vertical layer in which the sample(s) were collected
(EPI= epilimnion, META= metalimnion, HYP= hypolimnion).</td>
</tr>
<tr>
<td>total_biomass</td>
<td>numerical</td>
<td>milligrams per meter cubed</td>
<td>Total phytoplankton biomass concentration of all groups summed
(estimate; wet weight).</td>
</tr>
<tr>
<td>trophic_type</td>
<td>categorical</td>
<td>n/a</td>
<td>Feeding or nutritional strategy (autotroph, heterotroph, or
mixotroph).</td>
</tr>
<tr>
<td>variety</td>
<td>text</td>
<td>n/a</td>
<td>taxonomic sub-unit</td>
</tr>
<tr>
<td>volume_cell</td>
<td>numerical</td>
<td>micro-meters cubed</td>
<td>Mean volume of individual cells for each taxon.</td>
</tr>
<tr>
<td>volume_total</td>
<td>numerical</td>
<td>meters cubed</td>
<td>The total volume of the lake associated with the specified
monitoring_locaiton_name. The value is calculated via GIS tools based on
a raster DEM, which was produced using sonar data collected from
transects across the lake and using satellite imagery to trace the
lake's extent. Values are calculated to 0.01 metres cubed, but the error
would be greater than 1 (in most cases the DEM has 1 metre
resolution).</td>
</tr>
</tbody>
</table> 

## References

Nauwerk. A. 1963. Die Beziechungen Zwischen Zooplankton und
Phytotoplankton in see Erken. Symb. Bot. Ups. 17: 163p.

Shearer, J.A. 1978. Two devices for obtaining water samples from depth.
Can. J. Fish. Mar. Sewrv. Tech. Rep. 772: 9p.

Vollenweider, R.A. 1968. Scientific fundamentals of the eutrophication
of lakes and flowing waters, with particular reference to nitrogen and
phosphorus as factors in eutrophication. Tech. Rep. O.E.C.D. Paris
Das/CS1/68.27: 182 p.
