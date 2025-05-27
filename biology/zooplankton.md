# Zooplankton Data – Information Sheet

**Authors**: IISD Experimental Lakes Area, Michael Paterson, Patrique
Bulloch, Chris Hay

**Last Updated**: 2024-01-30

**Migrated By**: Delvin So

- [Zooplankton Data – Information Sheet](#zooplankton-data--information-sheet)
    - [General Background](#general-background)
    - [Considerations when using the ELA zooplankton data](#considerations-when-using-the-ela-zooplankton-data)
    - [Methods](#methods)
        - [Sampling](#sampling)
        - [Analysis](#analysis)
        - [Processing](#processing)
    - [Instrumentation](#instrumentation)
        - [Depth sounder](#depth-sounder)
        - [Zoonet](#zoonet)
        - [Salki Tube Zootube](#salki-tube-zootube)
        - [Zooplankton stations](#zooplankton-stations)
    - [Data Dictionary](#data-dictionary)
        - [List of columns by table](#list-of-columns-by-table)
        - [Column Definitions TBD](#column-definitions-tbd)
        - [Domains](#domains)
    - [References](#references)

<!-- /TOC -->
## General Background

*Zooplankton data have been collected from various lakes at the IISD Experimental Lakes Area (ELA), in Northwestern Ontario Canada since
1969. The collection of zooplankton samples was undertaken as part of
ELA’s Long-term Ecological Research (LTER) program and as supporting
data for various projects at the ELA. The methodology of sampling
changed several times from 1969-1979 and differs among lakes. The two
most commonly used sampling methods in current use (zoonets and Salki
tubes) were adopted for their respective suite of lakes in 1979 and 1988
respectively. After 1998, the final protocol change was made to lakes
sampled with zoonets to eliminate sampling at three depth zones in
favour of sampling the entire water column at once.*

*Zooplankton taxonomy and counts have been performed by various individuals, though considerable efforts have been made to minimize the
number of different analysts to reduce variability in the long-term record. Changes in taxonomic nomenclature and zooplankton identification
protocols have been tracked and, where necessary, taxonomy has been harmonized. The original designations used by different taxonomists are
also available. The datasets are being transferred from the Microsoft Access database to the Postgres master database.*

## Considerations when using the ELA zooplankton data

1.  Different methods have been used for collecting zooplankton in
    different lakes and at different times and they do not always
    provide comparable estimates of abundance (column entitled
    “method”). Samples collected using the Schindler -Patalas trap and
    various nets were collected at center-buoy only and comparisons
    suggest they provide similar results when integrated through the
    water column (Johannsson et al. 1992). Samples collected with the
    Salki-Patalas tubes were collected at multiple stations and the data
    are not directly relatable with data collected using the other
    methods. This problem is most concerning in Lakes 373 and 226 where
    both approaches were used at different times in the lakes’
    histories. Data from the different methods should be analysed
    separately.

2.  Different counting protocols have also been used over the years.
    Most importantly, there was a change in the way juvenile copepods
    were counted. Prior to 1998/99, juvenile copepods were only
    identified to group (calanoids, cyclopoids) and as early and later
    stages (c1-c3, c4-c5). After 1998/99, counters were asked to
    identify c4-c5 stages to species, if possible. As a result, counts
    of c4-c5 copepods IDed only to group typically drop to zero after
    1998/99 and species- level counts of c4-c5 copepods begin to show up
    in the data set. If you want comparable data through the entire
    period of record, it is necessary to throw out all the c4-5
    species-level data obtained post 1998/99 and combine c4-c5 counts at
    the group level. Adult copepods have been identified to species and
    sex in all samples.

3.  There have been changes in counters over the years. Occasionally,
    different counters may use different names for the same taxon. As a
    result, sudden change in a species occurrence may be associated with
    a change in counters (column entitled “counter”) rather than with an
    actual change in the species in the lake. Similarly, the same
    species may be given different names by different counters in
    different lakes. Especially problematic groups are
    *Eubosmina/Bosmina,* some of the *Daphnia* groups, and various
    rotifers. Date are available using either the original names
    provided by the counters or in a dataset where names have been
    harmonized as best as is possible.

4.  Not all counters identified rotifers (column entitled “Rotifers”; if
    code = 0, they weren’t counted).

5.  The data are all in numbers/L.

6.  Data are also available as biomass (ug/L). Biomass data were
    obtained by multiplying the density data by the average mass of
    different taxa and life stages. Mass data were obtained from
    length-weight regressions provided by Malley et al. (1989).
    Zooplankton in some samples were measured using a caliper and
    imaging system (ZEBRA). In other cases, individual masses were
    estimated from lake-specific data in Malley et al. (1989).

7.  Some samples were collected through the ice (column entitled Thin;
    code = 2). Since this was not done in all years, winter samples
    should be dropped to obtain comparable annual averages. Counts are
    typically very low in winter and skew the data if they aren’t
    removed. Thin = 1 means only a few samples were collected in a year
    and again the data are not suitable for generating annual estimates.
    Under-ice samples have all been collected using a net. For lakes
    sampled with a tube in the ice-free season, under-ice samples are
    not directly comparable for abundance estimates.

## Methods

### Sampling

As of 1998, lakes are usually sampled for zooplankton in one of two
ways. The first method is to perform two hauls with a double-barreled
zooplankton net (with a 53 µm mesh size) at centre buoy – the deepest
point in the lake (Figure 1). The second method uses Salki tubes, a 3”
diameter PVC tube which is lowered to a specified depth at 5-8 stations
distributed around the lake. The contents of the tube are filtered
through a 53 µm net into a 1L bottle to generate a composite sample from
all stations. Occasional samples have also been collected with a
Wisconsin-style plankton net (53 µm mesh). In the past, 76 µm nets were
sometimes used for tube samples (noted in the column titled mesh size).
Rotifers were not counted in these samples.

<img
src="./attachments/zooplankton/f9e6bf69ce2b8ae515e249095934e159e9f6f45e.jpg"
style="width:3.34375in;height:5in" />

Figure 1. Draining the contents of a zooplankton haul with the standard
ELA double-barrel net into a sampling container.

For all methods, samples were washed into 1L polyethylene bottles
containing 25 mL of methanol as a narcotizing agent (Gannon and Gannon
1975). Samples were immediately preserved upon return to the laboratory
with 100% sugar formalin. Prior to shipping for taxonomic and abundance
analyses, samples were filtered down to a final volume of 40 mL (if
possible), 2mL of which is sugar formalin (final formalin concentration
5%).

Depths were measured with a depth sounder at each sampling point (centre
buoy and/or zooplankton stations), and sampled depths were recorded.
Sampled depth and net or tube diameters were later used to estimate the
volume of lake water sieved by the net or tube assuming a net efficiency
of 100%. This information along with other metadata such as weather
conditions are entered into a digital database using Esri’s Survey123
application.

### Analysis

Typically, zooplankton were identified and enumerated from subsamples
that varied in size from 1/80 to all of the original sample, depending
on the abundance of the group. The entire sample volume is examined for
large crustaceans and for insects. A minimum of 300 microcrustacea,
excluding juvenile stages, are identified to species and sex. If an
identification problem arises, the organisms are picked out of the
sample and observed on a separate slide where they can be dissected and
manipulated. Free eggs and eggs attached to adult females are counted.

### Processing

Raw counts generated by the zooplankton taxonomists for each species are
stored into the database. Zooplankton taxa codes are also stored in the
database. Metadata previously entered into the Survey123 application are
used to calculate sampled volumes of lake water (pi*r^2 \* the depth
of the sample \* number of hauls, where r is the radius of the net or
tube). Count data and sample volumes are then used to calculate
abundance per litre (estimate of total abundance in the sample/ volume
of water sieved in the sample). Average species masses - determined
empirically by measuring many individuals of each of our zooplankton
species are used to estimate biomass per litre of each species of
zooplankton.

## Instrumentation

### Depth sounder

Depth sounders send a sound impulse through the water, which bounces
back to the device when it encounters a solid object (i.e. the lake
bottom). Depth sounders such as the Laylin SpeedTech SM-5 are used to
determine the total depth of the lake at the sampling station. A buffer
of ~1 m is subtracted from this depth to ensure the net does not contact
the lake bottom, stirring up sediments. This depth is the sampled depth
used to calculate sample volume.

### Zoonet

Most often, a double-barreled net is used as described by Chang et al.
(1980). Each net is built with a 12.7 cm diameter hoop affixed to a rope
marked in 0.5 m increments to control the sampling depth – ropes are
periodically re-marked or replaced due to stretching. For consistency, a
pair of nets (labelled for example 2024-L442-1 and 2024-L442-2) is
assigned to each lake for a period of two years before being replaced.
The net itself is a 53 µm mesh cone that terminates into a spigot
equipped with a ball valve. The spigot is installed by cutting a hole at
the bottom of the mesh cone, roughly the same size as the spigot
diameter. The spigot is secured into place with a hose clamp and
electrical tape. The end of the spigot that contacts the net is coated
in liquid electrical tape to blunt any edges that may create tears in
the mesh. Out of the water, the nets drain into the bottom of the net.
The net is rinsed and drained into a 1L bottle to collect the trapped
zooplankton. On occasion, some lakes have been sampled with a standard
Wisconsin zooplankton net (Wildco).

### Salki Tube (Zootube)

Zootubes are lengths of flexible 3” diameter PVC tubes long enough to
match the deepest point of their assigned lake (Salki 1993). For
consistency, one zootube is assigned to each lake sampled in this
manner, and each zootube is stored at its lake in a bin. A rope marked
with 0.5 m increments is affixed to the weighted distal end of the tube,
to control the sampling depth. The tubes are emptied into a 1L bottle by
funneling into a 53 µm mesh net to retain zooplankton, equipped with a
spigot and ball valve (see Zoonet description). For ease of handling,
this net is placed in a custom-made holder (a wooden plank with a hole
large enough to fit the filtering net) that is secured to the boat with
a clamp.

### Zooplankton stations

Zooplankton stations, like centre buoys that mark the deepest point in
the lake, are floats secured at different points in the lake that
correspond to different known depths. Each float consists of a buoy
equipped with a ring screw to allow mooring and is anchored to the lake
bottom with a cinder block or other heavy object (Campbell & Salki
1992). These are used to ensure consistency in spatial sampling, while
providing the added benefit of a secure anchorage to minimize boat
drift. Depths are always verified with a depth sounder to account for
changes in water level. In the absence of these stations, GPS
coordinates and one to two anchors are sufficient.

## Data Dictionary

### List of columns by table

Keys are indicated with asterisks (here they are compound keys with more
than one field)

Tabular Data – Phytoplankton Group Biomass and Total Biomass

• monitoring\_location\_name \*

• date\_collected\*

• stratum\*

• depth\_upper

• depth\_lower

• cyanobacteria

• chlorophyte

• euglenophyte

• chrysophyte

• diatoms

• cryptophyte

• dinoflagellate

• biomass\_total

Tabular Data – Phytoplankton Species Abundance, Biomass and Cell Volume

• monitoring\_location\_name \*

• date\_collected \*

• stratum\*

• depth\_upper

• depth\_lower

• species\_code\*

• volume\_cell

• density

• biomass

### Column Definitions (TBD)

### Domains

All date fields (activity\_end\_date, activity\_start\_date, and
update\_date) include year, month, and day in ISO 8601 format
(YYYY-MM-DD), but may be null (except for activity\_start\_date, which
is a key field).

Many of the metadata-related columns are derived from internal lookup
tables of a restricted list of values (dataset\_name,
method\_process\_description, method\_process\_detail,
method\_sample\_description, and method\_sample\_detail).

Most numeric values are rounded to two decimal points, but the true
degree of precision may be more coarse.

## References

Allen, G., N. D. Yan, and W. T. Geiling. 1994. ZEBRA2 - Zooplankton
enumeration and biomass routines for APIOS: A semi-automated sample
processing system for zooplankton ecologists. PIBS 2872.

Campbell, P., and A. G. Salki. 1992. A durable all-season marker float
and mooring buoy for limnological field studies. Canadian Technical
Report of Fisheries and Aquatic Sciences 1852.

Chang, P. S. S., D. F. Malley, W. J. Findlay, G. Mueller, and R. T.
Barnes. 1980. Species composition and seasonal abundance of zooplankton
in Lake 227, Experimental Lakes Area, northwestern Ontario, 1969-1978.
Canadian Data Report of Fisheries and Aquatic Sciences 182.

Gannon, J. E., and S. A. Gannon. 1975. Notes on the narcotization of
crustacean zooplankton. Crustaceana 28:220-224.

Johannsson, O. E., M. A. Shaw, N. D. Yan, J.-M. Filion, and D. F.
Malley. 1992. A comparison of freshwater zooplankton sampling gear:
Nets, traps, and submersible pump. Canadian Technical Report of
Fisheries and Aquatic Sciences 1894.

Malley, D. F., S. G. Lawrence, M. A. MacIver, and W. J. Findlay. 1989.
Range of variation in estimates of dry weight for planktonic Crustacea
and Rotifera from temperate North American lakes. Canadian Technical
Report of Fisheries and Aquatic Sciences 1666.

Nauwerk. A. 1963. Die Beziechungen Zwischen Zooplankton und
Phytotoplankton in see Erken. Symb. Bot. Ups. 17: 163p.

Salki, A. G. 1993. Lake variation and climate change study: VII.
Crustacean plankton of a lake flushing rate series in the Experimental
Lakes Area, northwestern Ontario, 1987-1990. Canadian Data Report of
Fisheries and Aquatic Sciences 880.

Shearer, J.A. 1978. Two devices for obtaining water samples from depth.
Can. J. Fish. Mar. Sewrv. Tech. Rep. 772: 9p.

Vollenweider, R.A. 1968. Scientific fundamentals of the eutrophication
of lakes and flowing waters, with particular reference to nitrogen and
phosphorus as factors in eutrophication. Tech. Rep. O.E.C.D. Paris
Das/CS1/68.27: 182 p.
