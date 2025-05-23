 

**Authors:** IISD Experimental Lakes Area, Sonya Havens, Chris Hay, Ken
Sandilands, Paul Fafard, Idil Yaktubay 

**Last Updated:** 2025-05-23

**Last Updated by**: Chris Hay

# Contents

[General Information [2](#general-information)](#general-information)

[Methods [2](#methods)](#methods)

[Sampling [2](#sampling)](#sampling)

[Integrated Water Sampling
[2](#integrated-water-sampling)](#integrated-water-sampling)

[Profile Sampling [3](#profile-sampling)](#profile-sampling)

[Analysis [3](#analysis)](#analysis)

[Processing [4](#processing)](#processing)

[Instrumentation [5](#instrumentation)](#instrumentation)

[Data Dictionary [5](#data-dictionary)](#data-dictionary)

[List of columns by table
[5](#list-of-columns-by-table)](#list-of-columns-by-table)

[Column Definitions [6](#column-definitions)](#column-definitions)

[References [12](#references)](#references)

[Appendices [13](#appendices)](#appendices)

[Result Detection Limits
[13](#result-detection-limits)](#result-detection-limits)

[Quality Control Levels
[13](#quality-control-levels)](#quality-control-levels)

[Chemical Parameter Names on EDI and DataStream
[14](#chemical-parameter-names-on-edi-and-datastream)](#chemical-parameter-names-on-edi-and-datastream)

# General Information 

Chemistry data from the Experimental Lakes Area (ELA) has been collected
across ELA lakes since May 1968. Water samples are collected and
analyzed for a variety of parameters, for both specific research
projects and long-term ecological research (LTER), and across
manipulated lakes or enclosures and reference lakes.    
   
The management of the chemistry dataset has periodically changed since
its inception, as would be expected with technological advances over the
years. Currently, all chemistry data undergo ETL (extract, transform,
load) from source databases into a PostgreSQL master database. This
represents a merging of older chemistry data 1968 through 2016 that were
compiled into a Microsoft Access database and newer data 2017 to present
which are managed in Sample Master (a Laboratory Information Management
System). 

 

The way fields are named and formatted, as well as the naming of
chemical parameters, is largely based on the DataStream Open Data Schema
for Water Quality Data, which is itself based on the United States
Environmental Protection Agency’s “Water Quality eXchange” (WQX)
(DataStream 2022; United States Environmental Protection Agency 2022).
However, the names of a few chemical parameters in the internal IISD-ELA
Master Database and the Chemistry of LTER Lakes data package on the
Environmental Data Initiative (EDI) repository differ from those used in
the parallel data package on the DataStream repository. For further
details on these differences, refer to the Appendices section.

# Methods 

## Sampling

### Integrated Water Sampling

Integrated water samples were collected from the epilimnion and
metalimnion (when present) of LTER lakes approximately biweekly during
the open water season (c. May through October). See the
“Instrumentation” section for a diagram of the integrated sampler used.

Integrated epilimnion samples (**EPI**) are collected starting from the
lake surface to 0.5 m above the bottom of the thermal epilimnion, or to
the depth of 1% of surface PAR when the thermal epilimnion extends
beyond this depth by at least 0.5 m. The thermal epilimnion has stable
temperature throughout, with changes in temperature of less than 1 °C /
1 m increase in depth. The bottom of the thermal epilimnion is defined
as the shallowest depth with a stable temperature, after which a
temperature change of ≥ 0.25 °C occurs within a 0.25 m increase in
depth.  

 

Integrated metalimnion samples (**META**) are collected between the
bottom of the thermal epilimnion and the depth at which 1% of surface
PAR occurs. When the thermal epilimnion extends beyond the depth of 1%
of surface PAR, no integrated metalimnion sample is collected. When
taking a META sample, the inlet tube is closed off using the clamping
mechanism before entering the water and later opened via a messenger
weight when at the proper depth. In this way, epilimnetic water is not
inadvertently sampled as the sampler descends to the proper sampling
depth of the metalimnion. 

 

### Profile Sampling 

Water chemistry profile sampling involves taking samples of the water
column at pre-determined depths (e.g. Lake 239 depths are 1, 5, 10, 15,
20, 25, 30 m). Note that if an integrated epilimnion sample was
collected at the same time as the profile samples (and usually this is
the case, for IISD-ELA data), additional profile samples within the
epilimnion are not collected as well. Profile samples within the
epilimnion range would be essentially a repeat sample of the same water
as the integrated epilimnion sample, since the epilimnion is well mixed
and homogeneous, at least in terms of chemistry. This was tested
historically and generally holds true, except on very calm (non-windy)
days. It saves a lot on chemistry costs and effort for IISD-ELA.

So for example, if you are looking to use profile data from 239 and see
the depths only begin at 5 m (missing a 1 m sample), it means you will
need to also use the integrated epilimnion data to represent the first
layer within the profile data.

Water is pumped from depth using a marked sampling line (Kuri Tec
KLEARON food grade PVC tubing: 1/4'” inner diameter, 3/8” outer diameter
for the marked line and 3/16” inner diameter, 5/16” outer diameter to
connect the line to the pump), and a 24v Greylor gear pump (part number:
001-240103 - 24V, HDPE Gears, Heat Sink w/No Holes, Viton Seal). The
pump must not be run dry- the gears will melt and cause the pump to stop
working properly.  

 

While sampling with the pump, care is taken to ensure that the pump does
not introduce air (bubbles) to the sample. The connection between the
pump hose and the sampling line is inspected to ensure air is not being
introduced, and the out-line of the pump is also inspected for bubbles.
If bubbles are present in the out-line but not the in-line, this
indicates that the seals on the pump need to be replaced.  

Bottles are rinsed twice with water from the target depth before
filling, and when filling a bottle for analysis that is sensitive to air
being introduced (e.g. an oxygen bottle) the hose from the pump is
inserted to the bottom of the bottle during filling, to reduce air being
mixed into the sample. 

 

## Analysis 

Sample bottles are brought to the IISD-ELA chemistry lab on site, and
subsampled for lab analyses for a wide variety of parameters. Sometimes
samples have been shipped to other labs for certain analyses, but
increasingly analysis is done at the IISD-ELA chemistry lab. The lab
that performed analysis on a sample is indicated in the lab name column
for each record in the data. 

 

Methods and instrumentation used to analyze samples have changed over
the decades of data in the IISD-ELA chemistry dataset. This is indicated
in the data via method name and instrument columns. Details of
laboratory procedures for each parameter are described in published
standard operating procedures—editions of The Chemical Analysis of Fresh
Water (Havens et al. 2024; Stainton et al. 1977). The year and edition
are indicated in the analytical reference column for each record in the
data. Early data have unknown processing methods. 

 

## Processing 

Benchtop quality control practices are carried out as described in the
standard operating procedures. Data are entered into Sample Master (the
chemistry lab LIMS) and undergo some additional quality control checks
and corrections when traveling through the pipeline loading the data
into the IISD-ELA master database. These are checks that values are
within expected ranges, and that metadata-related columns are populated
or conform to expected values. The data are otherwise relatively “raw”
and unprocessed.

# Instrumentation 

<img src="attachments/media/image1.png"
style="width:6.47591in;height:5.53797in"
alt="A diagram of a machine Description automatically generated" /> 

This is the original Integrated Sampler design (Shearer 1978), used for
integrated water samples. The overall design has remained largely
unchanged since its inception. The sample bottle is now a ~2 L Nalgene
bottle encased and insulated within a large PVC shell, and the
weight/bottle holder is constructed of a single piece of a solid
stainless steel. The frame with the clamping mechanism clips into the
weight/bottle holder with small metal clips, rather than wing-nuts. 

# Data Dictionary 

## List of columns by table 

Tabular Data – Chemistry of LTER Lakes 

- dataset_name 

<!-- -->

- monitoring_location_id 

<!-- -->

- monitoring_location_name 

<!-- -->

- activity_media_name 

<!-- -->

- activity_start_date 

<!-- -->

- activity_start_time 

<!-- -->

- activity_end_date 

<!-- -->

- activity_end_time 

<!-- -->

- activity_depth_height_measure 

<!-- -->

- activity_depth_height_unit 

<!-- -->

- layer_collection_end_depth 

<!-- -->

- layer_collection_start_depth 

<!-- -->

- characteristic_name 

<!-- -->

- characteristic_name_long 

<!-- -->

- method_speciation 

<!-- -->

- result_sample_fraction 

<!-- -->

- result_value 

<!-- -->

- result_unit 

<!-- -->

- result_detection_quantitation_limit_measure 

<!-- -->

- result_detection_quantitation_limit_unit 

<!-- -->

- result_detection_quantitation_limit_type 

<!-- -->

- result_status_id 

<!-- -->

- analysis_start_date 

<!-- -->

- result_analytical_method_name 

<!-- -->

- result_analytical_method_instrument 

<!-- -->

- result_analytical_reference_method 

<!-- -->

- laboratory_name 

<!-- -->

- laboratory_sample_id 

<!-- -->

- field_comment 

<!-- -->

- analysis_comment 

<!-- -->

- result_comment 

## Column Definitions

<table>
<colgroup>
<col style="width: 18%" />
<col style="width: 15%" />
<col style="width: 11%" />
<col style="width: 54%" />
</colgroup>
<thead>
<tr>
<th><strong>Column name (alphabetical)</strong></th>
<th style="text-align: center;"><strong>data type</strong></th>
<th style="text-align: center;"><strong>unit</strong></th>
<th><strong>definition</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td>activity_depth_<br />
height_measure</td>
<td style="text-align: center;">numeric</td>
<td style="text-align: center;">See "activity_<br />
depth_<br />
height_<br />
unit"</td>
<td>The depth the sample was collected, measured down from the surface
of the lake. For the associated unit, see "activity_depth_height_unit".
Sometimes samples are collected at discrete profile depths, in which
case the specific numeric level is indicated here. If an integrated
sample was collected, this field is left as null, the layer name is
indicated in another column ("activity_depth_height_unit", e.g. "epi"),
and the start and end depth are indicated (when available) elsewhere in
other columns ("layer_collection_start/end_depth").</td>
</tr>
<tr>
<td>activity_depth_<br />
height_unit</td>
<td style="text-align: center;">character varying</td>
<td style="text-align: center;">N/A </td>
<td>The unit associated with the depth value
(“activity_depth_height_measure”), e.g., “m” for metres, if the depth
value was a specific numeric level. If the sample is not from a numeric
depth but an integrated sample from a layer of the lake, this field will
note the stratification layer (epilimnion, metalimnion, hypolimnion), or
a “surface grab” if the sample was collected from reaching an arm into
the surface of the water, or “eup” for the euphotic zone (referring to
the top part of the lakes that has sufficient light for algal growth,
usually anything greater than 1% surface light).</td>
</tr>
<tr>
<td><p>activity_end_</p>
<p>date</p></td>
<td style="text-align: center;">date</td>
<td style="text-align: center;"> N/A</td>
<td>Date field sampling or surveying activity ended (YYYY-MM-DD). Null
or blank values may indicate the end date was the same day, or in rare
cases that the end date is unknown. See the associated info sheet for
more information on sampling protocols.</td>
</tr>
<tr>
<td><p>activity_end_</p>
<p>time</p></td>
<td style="text-align: center;">time without time zone</td>
<td style="text-align: center;"> N/A</td>
<td>Time field sampling or surveying activity ended.</td>
</tr>
<tr>
<td>activity_media_<br />
name</td>
<td style="text-align: center;">character varying</td>
<td style="text-align: center;"> N/A</td>
<td>Describes what type of material was sampled.</td>
</tr>
<tr>
<td><p>activity_start_</p>
<p>date</p></td>
<td style="text-align: center;">date</td>
<td style="text-align: center;"> N/A</td>
<td>Date field sampling or surveying activity began (YYYY-MM-DD).</td>
</tr>
<tr>
<td><p>activity_start_</p>
<p>time</p></td>
<td style="text-align: center;">time without time zone</td>
<td style="text-align: center;"> N/A</td>
<td>Time field sampling or surveying activity began.</td>
</tr>
<tr>
<td><p>analysis_</p>
<p>comment</p></td>
<td style="text-align: center;">character varying</td>
<td style="text-align: center;">N/A </td>
<td>A comment about the analysis of the sample (lab work). If the
comment starts with "Sample note: ", the value is a historical comment
(pre-2017) related to the entire sample, rather than to the
characteristic specified by the row. Therefore, the entry may only
pertain to certain parameters measured on that sample, and may or may
not be related to that particular row.</td>
</tr>
<tr>
<td><p>analysis_start_</p>
<p>date</p></td>
<td style="text-align: center;">date</td>
<td style="text-align: center;"> N/A</td>
<td>The date on which sample analysis started (YYYY-MM-DD).</td>
</tr>
<tr>
<td><p>characteristic_</p>
<p>name</p></td>
<td style="text-align: center;">character varying</td>
<td style="text-align: center;"> N/A</td>
<td>The parameter being measured (abbreviated version). For chemistry,
usually the element in question (e.g., "Fe").</td>
</tr>
<tr>
<td>characteristic_<br />
name_long</td>
<td style="text-align: center;">character varying</td>
<td style="text-align: center;"> N/A</td>
<td>The full, non-abbreviated version of the parameter being measured.
For example, for chemistry, usually the full name of the element in
question (e.g., Iron, rather than Fe).</td>
</tr>
<tr>
<td>dataset_name</td>
<td style="text-align: center;">character varying</td>
<td style="text-align: center;"> N/A</td>
<td>Name of the dataset. A dataset is a collection of data to which
several individual data records (rows) belong. Dataset names are useful
to distinguish groups of data across different research fields and
provide some descriptive context.</td>
</tr>
<tr>
<td>field_comment</td>
<td style="text-align: center;">character varying</td>
<td style="text-align: center;"> N/A</td>
<td>Any kind of comment from when in the field, related to acquiring the
sample (vs. result_comment, which is noted at a later stage). May be an
important caveat to analysis of the data (e.g., notes about the rain
gauge overflowing, which affects accuracy of precip_rain_gauge_mm
value).</td>
</tr>
<tr>
<td><p>laboratory_</p>
<p>name</p></td>
<td style="text-align: center;">character varying</td>
<td style="text-align: center;"> N/A</td>
<td>Theoretically this column is defined as the name of the laboratory
that conducted the analysis on the sample in question, but in actuality
this column does not always fit such a clean-cut definition.
Historically the use of this field has not been standardized, so values
may be a name of an individual, institution, or location. In recent
years, the column value is usually "bcooney", referring to an IISD-ELA
staff working at the IISD-ELA chemistry lab. Note that although many
samples are analyzed by IISD-ELA, some samples are shipped to external
labs for certain analyses (e.g., The University of Alberta
Biogeochemical Analytical Service Laboratory). There are future plans to
improve the data quality of the values in this column.</td>
</tr>
<tr>
<td>laboratory_<br />
sample_id</td>
<td style="text-align: center;">character varying</td>
<td style="text-align: center;"> N/A</td>
<td>A unique code for each sample, at least for 2017 to present data
obtained from the LIMS. Note that each sample is typically analyzed for
multiple parameters. The ID usually begins with the date the sample was
logged in at the lab (e.g., 2022051101-01 for May 11th, 2022).</td>
</tr>
<tr>
<td><p>layer_</p>
<p>collection_<br />
end_depth</p></td>
<td style="text-align: center;">numeric</td>
<td style="text-align: center;">metres</td>
<td>Along with “layer_collection_start_depth”, this field is mostly used
for 2017 to present year data when an integrated sample was collected,
to specify the range of the layer that the sample was collected within.
For example, a record with layer_collection_start_depth = 0.00,
layer_collection_end_depth = 5.50, and activity_depth_height_unit = epi,
indicates an integrated sample from an epilimnion layer defined as 0m to
5.5m depth from the surface of the lake.</td>
</tr>
<tr>
<td><p>layer_</p>
<p>collection_<br />
start_depth</p></td>
<td style="text-align: center;">numeric</td>
<td style="text-align: center;">metres</td>
<td>Along with “layer_collection_end_depth”, this field is mostly used
for 2017 to present year data when an integrated sample was collected,
to specify the range of the layer that the sample was collected within.
For example, a record with layer_collection_start_depth = 0.00,
layer_collection_end_depth = 5.50, and activity_depth_height_unit = epi,
indicates an integrated sample from an epilimnion layer defined as 0m to
5.5m depth from the surface of the lake.</td>
</tr>
<tr>
<td><p>method_</p>
<p>speciation</p></td>
<td style="text-align: center;">character varying</td>
<td style="text-align: center;"> N/A</td>
<td>How the parameter specified by the characteristic name in the
associated row is described in method.</td>
</tr>
<tr>
<td>monitoring_<br />
location_id</td>
<td style="text-align: center;">uuid</td>
<td style="text-align: center;"> N/A</td>
<td>A uuid for each monitoring_location_name, used for internal database
table joining purposes.</td>
</tr>
<tr>
<td>monitoring_<br />
location_name</td>
<td style="text-align: center;">character varying</td>
<td style="text-align: center;"> N/A</td>
<td>Name of sampled or surveyed geographic location at the IISD
Experimental Lakes Area field site. The name consists of: &lt;location
sublocation station&gt;. Location is typically the lake number (each
lake is named with a number, representing the lake's geographical
watershed), sublocation which typically specifies LA for "lake" (or a
basin, e.g. NB - north basin, or other), and station which is usually CB
("centre buoy" - at about the deepest point of the lake).</td>
</tr>
<tr>
<td><p>result_</p>
<p>detection_<br />
quantitation_</p>
<p>limit_measure</p></td>
<td style="text-align: center;">numeric</td>
<td style="text-align: center;"><p>See "result_</p>
<p>detection_quantitation_limit_unit"</p></td>
<td>The result detection limit value. The associated unit is in the
field "result_detection_quantitation_limit_unit". In the chemistry
dataset, detection limits vary for a number of reasons including the
changes in instrumentation over the years and a shift since 2017 to
assessing them each sample run. There are a number of potential
approaches to assessing the detection limits (e.g. half the limit,
normal distribution of the detection limit), but we cannot be
proscriptive for how individuals use our data. For earlier years of data
(1968-2016) we are lacking documentation on how detection limits were
calculated. For more information about how detection limits were
calculated for 2017-2022 data, see the chem info sheet appendices.</td>
</tr>
<tr>
<td><p>result_</p>
<p>detection_<br />
quantitation_</p>
<p>limit_unit</p></td>
<td style="text-align: center;">character varying</td>
<td style="text-align: center;"> N/A</td>
<td>A field for the unit associated with
"result_detection_quantitation_limit_measure". Always identical to the
result_unit value (at least for the chemistry dataset 2017 to
Present).</td>
</tr>
<tr>
<td><p>result_</p>
<p>detection_<br />
quantitation_</p>
<p>limit_type</p></td>
<td style="text-align: center;">character varying</td>
<td style="text-align: center;"> N/A</td>
<td>For all IISD-ELA Chemistry data (at least 2017 to Present), it is
always “Method Detection Level” (United States Environmental Protection
Agency 2017; i.e., “Limit of Detection”). That is, not the “Limit of
Quantitation” which is 3.3 times the “Limit of Detection”.</td>
</tr>
<tr>
<td><p>result_</p>
<p>analytical_<br />
method_name</p></td>
<td style="text-align: center;">character varying</td>
<td style="text-align: center;"> N/A</td>
<td>The short name for the analytical method used (e.g., ELA-PartP,
UA-ClSO4, etc.). The prefix is the specific institution associated with
the method (e.g., ELA = Experimental Lakes Area, UA = University of
Alberta).For pre-2017 data, this value may not be available. In this
case, ‘N/A’ (not available) was entered.</td>
</tr>
<tr>
<td><p>result_</p>
<p>analytical_<br />
method_</p>
<p>instrument</p></td>
<td style="text-align: center;">character varying</td>
<td style="text-align: center;"> N/A</td>
<td>The instrument (tool) used to analyze the sample (e.g., Dionex
DX-600 Ion Chromatography, Fisher Scientific Accumet pH meter,
Cole-Parmer 2100 Spectrophotometer, etc.). Instrumentation cannot be
assumed to be the same within certain time periods or
characteristic_name values. For example, it is possible that two
different instruments may be used in a given year, if one breaks down
and an alternate is needed. For 2017 to present data, the instrument
used is recorded for every sample or test, so be aware that it may
change from record to record. For pre-2017 data, this value may not be
available. In this case, ‘N/A’ (not available) was entered.</td>
</tr>
<tr>
<td><p>result_</p>
<p>analytical_<br />
reference_</p>
<p>method</p></td>
<td style="text-align: center;">character varying</td>
<td style="text-align: center;"> N/A</td>
<td>The standard operating procedure reference for details on analytical
methods. This is useful for finding additional information for better
understanding results, and as a reference when publishing research using
the data. Typically this is a specific edition of "The Chemical Analysis
of Fresh Water". The intention is that this will be updated and
published on a more frequent basis than in the past, to reflect changing
instruments and methods.</td>
</tr>
<tr>
<td>result_comment</td>
<td style="text-align: center;">character varying</td>
<td style="text-align: center;"> N/A</td>
<td>Notes about the result. This field is rarely used. Comments were
seemingly noted at later analysis or quality control stages (vs.
field_comment, which was collected while in the field). E.g., “Trend
analysis shows the result to be an outlier and possibly erroneous.” Or
“This value is the average of two instrument duplicate measurements
which were not within 5% (281 vs 265 ug/L). The logic is that assuming
one of these is the true value, the average value will be within 3% of
it.”</td>
</tr>
<tr>
<td>result_sample_<br />
fraction</td>
<td style="text-align: center;">character varying</td>
<td style="text-align: center;"> N/A</td>
<td>Describes the portion of the characteristic being analyzed.</td>
</tr>
<tr>
<td>result_status_id</td>
<td style="text-align: center;">character varying</td>
<td style="text-align: center;"> N/A</td>
<td>Provides a level of quality control that the record has undergone
(thus, “trust” in the data). Note that this only applies for data 2017
to Present. There are three levels. See descriptions for each of these
levels in the appendices of the chem info sheet. Note that IISD-ELA’s
quality control management extends beyond the factors considered for
this field. For example, IISD-ELA carries out benchtop quality control
practices, which are stipulated in each test’s standard operating
procedure.</td>
</tr>
<tr>
<td>result_unit</td>
<td style="text-align: center;">character varying</td>
<td style="text-align: center;"> N/A</td>
<td>Units of measure for the result value, associated with the
characteristic name parameter.</td>
</tr>
<tr>
<td>result_value</td>
<td style="text-align: center;">numeric</td>
<td style="text-align: center;">See "result_<br />
unit"</td>
<td>The actual measured number for the parameter: the result. Basically,
this is the meaningful number measured or determined for the parameter
in question. For the associated unit, see "result_unit". For more
information, read the definition for the
"result_detection_quantitation_limit_measure" column and read in the
chem info sheet appendices an important bolded note about below
detection scenarios.</td>
</tr>
</tbody>
</table>

# References

DataStream. 2022. DataStream Open Data Schema for Water Quality Data –
JSON Schema. <https://github.com/datastreamapp/schema>

DataStream. 2025. Welcome to DataStream’s learning centre!

> <https://datastream.org/en-ca/documentation>

Havens, S.M., M.P. Stainton, and B.C. Cooney. 2024. The Chemical
Analysis of Fresh Water – Third Edition. International Institute for
Sustainable Development.
<https://www.iisd.org/publications/guide/chemical-analysis-fresh-water-third-edition>
DOI: <https://dx.doi.org/10.13140/RG.2.2.32178.82889>

Shearer, J.A. 1978. Two devices for obtaining water samples integrated
over depth. Can. Fish. Mar. Serv. Tech. Rep. 772: iv+9p.

Stainton, M.P., M.J. Capel, and F.A.J. Armstrong. 1977. The Chemical
Analysis of Fresh Water, 2<sup>nd</sup> ed. Fish. Mar. Serv. Misc. Spec.
Publ. 25:116 p. <https://waves-vagues.dfo-mpo.gc.ca/Library/110147.pdf>

United States Environmental Protection Agency. 2017. WQXWeb Template
Dictionary v3.xls (Sheet: WQX Web Allowable Values) from
wqxweb3_physical_chemical_package_0.zip on page Water Quality Exchange
Web Template Files. Last saved 2017-07-06.
<https://www.epa.gov/waterdata/water-quality-exchange-web-template-files>

United States Environmental Protection Agency. 2022. Characteristic.CSV.
from WQX Domain Value Services and Downloads. Last modified 2022-05-31.
<https://www.epa.gov/waterdata/storage-and-retrieval-and-water-quality-exchange-domain-services-and-downloads>

# Appendices

## Result Detection Limits

The result detection limit values
(result_detection_quantitation_limit_measure) from 2017 to present were
calculated as follows:

- Initially average detection limits were calculated and applied as
  annual averages per parameter (characteristic_name), but these were
  all changed-over to be detection limits per run, by the end of 2024.
  Given the finer scale of analytical run detection limits, the data
  user can average per year or summarize whichever way they deem fit.

- Whether a result value is above or below detection is determined at
  the time of data entry. If the result is below detection, typically
  the result_value is entered as 0, but sometimes the actual (below
  detection) value is noted instead. **It is up to the data user to
  examine the result_value vs. detection limit and decide how they will
  handle below detection records.**

- A description of how the detection limit is calculated is described in
  the third edition of The Chemical Analysis of Freshwater (Havens et
  al. 2024). It is calculated for each run by using equations 1 through
  3:

> Equation 1.          $`C_{dl} = \ \frac{y_{d} - b}{m}`$
>
> where *b* is the y-intercept, *m* is the slope, and *y<sub>d</sub>* is
> the signal detection limit, which is calculated using equation 2:
>
> Equation. 2.         $`y_{d} = 3s_{y} + b`$
>
> where *s<sub>y</sub>* is the residuals between the measured signal for
> each standard concentration and the calibration curve predicted
> response for each standard concentration and is calculated using
> equation 3:
>
> Equation 3.         
> $`s_{y} = \ \sqrt{\frac{?_{}^{}{di}^{2}}{n - 2}}`$
>
> where *n* is the number of standards in the calibration curve, and
> *di* is the difference between the measured signal for each standard
> concentration and the calibration curve predicted response for each
> standard concentration.

## Quality Control Levels

- Preliminary: Samples that have passed the analytical quality control
  parameters (samples that failed are not entered into the database).
  Quality control parameters for each analysis are available in the
  third edition of The Chemical Analysis of Fresh Water (Havens et al.
  2024). This step is benchmark quality control (e.g., blanks,
  duplicates, etc.). Internally this corresponds with level
  result_status_id 1 in Sample Master and “Entered”.

- Accepted: Samples that have undergone a second level of quality
  control. That is, records that have passed trend analysis. Trend
  analysis is conducted for each parameter at each site to look for
  outliers and then investigate the outliers. This step is done
  internally using an R script for efficiency. For more information, see
  the third edition of The Chemical Analysis of Fresh Water (Havens et
  al. 2024). Internally this corresponds with level result_status_id 2
  in Sample Master and “Validated”.

- Final: Samples that have undergone external peer-review. Currently
  IISD-ELA has not yet defined a process to evaluate whether a record
  has been peer-reviewed, but there are plans to do this and use this
  designation in the future. Internally this corresponds with level
  result_status_id 3 in Sample Master and “Approved”.

- Not noted or null: Quality control level is not noted for all pre-2017
  records. For 2017 to present, records with result_status_id 0 or null
  are not written to the database, as the result value has not been
  entered yet (though other parameters for a record may be filled out
  ahead of time in Sample Master).

## Chemical Parameter Names on EDI and DataStream

Following a discussion in early 2025 between DataStream staff and
IISD-ELA’s data team and research chemist, the names of chemical
parameters in both the IISD-ELA master database and the Chemistry of
LTER Lakes data package on EDI were revised to better align with those
used in the parallel DataStream data package (see table below). However,
we decided to keep some differences.

The result sample fractions for “PARTC” and “PARTFE” were labeled as
“Suspended” across EDI, the IISD-ELA master database, and DataStream,
following DataStream’s guidance for non-nutrient parameters. However, we
thought the “Suspended” label may cause confusion since these
measurements actually refer to particles retained on a filter. To
address this, the parameter names on EDI and in the IISD-ELA master
database are “particulate,” but it is “suspended” on DataStream (their
standards must be followed for the data upload to be accepted for their
repository). A similar clarification was made for “PARTN” and “PARTP”,
although their result sample fraction labels already make this clear.

In the EDI data package and the IISD-ELA master database, each chemical
parameter has a unique name in the characteristic columns. In contrast,
on DataStream, parameters are distinguished by unique combinations of
CharacteristicName, MethodSpeciation, and ResultSampleFraction. For
example, our “Nitrogen, particulate” and “Total dissolved nitrogen” are
both labeled as “Total Nitrogen, mixed forms” on DataStream, but are
differentiated by their ResultSampleFraction values: “Non-Filterable
(Particle)” and “Filtered,” respectively. Therefore, it is important to
consider all three columns when interpreting the DataStream data
package.

For more information, please refer to DataStream’s learning centre
website (DataStream 2025) and to *The Chemical Analysis of Fresh Water*
(Havens et al. 2024).

<table>
<colgroup>
<col style="width: 2%" />
<col style="width: 11%" />
<col style="width: 19%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 21%" />
<col style="width: 9%" />
<col style="width: 11%" />
</colgroup>
<thead>
<tr>
<th style="text-align: center;"></th>
<th colspan="4" style="text-align: center;"><strong>EDI Repository and
IISD-ELA Database</strong></th>
<th colspan="3" style="text-align: center;"><strong>DataStream
Repository</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td style="text-align: center;"></td>
<td><strong>characteristic_name</strong></td>
<td><strong>characteristic_name_long</strong></td>
<td><strong>method_speciation</strong></td>
<td><strong>result_sample_fraction</strong></td>
<td><strong>CharacteristicName</strong></td>
<td><strong>MethodSpeciation</strong></td>
<td><strong>ResultSampleFraction</strong></td>
</tr>
<tr>
<td style="text-align: right;">1</td>
<td>A254</td>
<td>Specific UV Absorbance at 254 nm</td>
<td> </td>
<td>Filtered, lab</td>
<td>Specific UV Absorbance at 254 nm</td>
<td> </td>
<td>Filtered, lab</td>
</tr>
<tr>
<td style="text-align: right;">2</td>
<td>ALK</td>
<td>Alkalinity, total</td>
<td> </td>
<td> </td>
<td>Alkalinity, total</td>
<td> </td>
<td> </td>
</tr>
<tr>
<td style="text-align: right;">3</td>
<td>CA</td>
<td>Calcium</td>
<td> </td>
<td>Dissolved</td>
<td>Calcium</td>
<td> </td>
<td>Dissolved</td>
</tr>
<tr>
<td style="text-align: right;">4</td>
<td>CHLA</td>
<td>Chlorophyll a, uncorrected for pheophytin</td>
<td> </td>
<td> </td>
<td>Chlorophyll a, uncorrected for pheophytin</td>
<td> </td>
<td> </td>
</tr>
<tr>
<td style="text-align: right;">5</td>
<td>CL</td>
<td>Chloride</td>
<td> </td>
<td>Dissolved</td>
<td>Chloride</td>
<td> </td>
<td>Dissolved</td>
</tr>
<tr>
<td style="text-align: right;">6</td>
<td>COLOUR</td>
<td>Colour</td>
<td> </td>
<td> </td>
<td>Color</td>
<td> </td>
<td> </td>
</tr>
<tr>
<td style="text-align: right;">7</td>
<td>COND</td>
<td>Conductivity</td>
<td> </td>
<td> </td>
<td>Conductivity</td>
<td> </td>
<td> </td>
</tr>
<tr>
<td style="text-align: right;">8</td>
<td>DIC</td>
<td>Inorganic carbon</td>
<td> </td>
<td>Dissolved</td>
<td>Inorganic carbon</td>
<td> </td>
<td>Dissolved</td>
</tr>
<tr>
<td style="text-align: right;">9</td>
<td>DOC</td>
<td>Organic carbon</td>
<td> </td>
<td>Dissolved</td>
<td>Organic carbon</td>
<td> </td>
<td>Dissolved</td>
</tr>
<tr>
<td style="text-align: right;">10</td>
<td>FE</td>
<td>Iron</td>
<td> </td>
<td>Dissolved</td>
<td>Iron</td>
<td> </td>
<td>Dissolved</td>
</tr>
<tr>
<td style="text-align: right;">11</td>
<td>K</td>
<td>Potassium</td>
<td> </td>
<td> </td>
<td>Potassium</td>
<td> </td>
<td> </td>
</tr>
<tr>
<td style="text-align: right;">12</td>
<td>MG</td>
<td>Magnesium</td>
<td> </td>
<td>Dissolved</td>
<td>Magnesium</td>
<td> </td>
<td>Dissolved</td>
</tr>
<tr>
<td style="text-align: right;">13</td>
<td>MN</td>
<td>Manganese</td>
<td> </td>
<td>Dissolved</td>
<td>Manganese</td>
<td> </td>
<td>Dissolved</td>
</tr>
<tr>
<td style="text-align: right;">14</td>
<td>NA</td>
<td>Sodium</td>
<td> </td>
<td>Dissolved</td>
<td>Sodium</td>
<td> </td>
<td>Dissolved</td>
</tr>
<tr>
<td style="text-align: right;">15</td>
<td>NH3</td>
<td>Ammonia</td>
<td>as N</td>
<td>Filtered, lab</td>
<td>Ammonia</td>
<td>as N</td>
<td>Filtered, lab</td>
</tr>
<tr>
<td style="text-align: right;">16</td>
<td>NO2</td>
<td>Nitrite</td>
<td>as N</td>
<td>Filtered, lab</td>
<td>Nitrite</td>
<td>as N</td>
<td>Filtered, lab</td>
</tr>
<tr>
<td style="text-align: right;">17</td>
<td>NO3</td>
<td>Nitrate</td>
<td>as N</td>
<td>Filtered, lab</td>
<td>Nitrate</td>
<td>as N</td>
<td>Filtered, lab</td>
</tr>
<tr>
<td style="text-align: right;">18</td>
<td>O2</td>
<td>Dissolved oxygen (DO)</td>
<td> </td>
<td> </td>
<td>Dissolved oxygen (DO)</td>
<td> </td>
<td> </td>
</tr>
<tr>
<td style="text-align: right;">19</td>
<td>PARTC</td>
<td>Carbon, particulate</td>
<td> </td>
<td>Suspended</td>
<td>Organic carbon</td>
<td> </td>
<td>Suspended</td>
</tr>
<tr>
<td style="text-align: right;">20</td>
<td>PARTFE</td>
<td>Iron, particulate</td>
<td> </td>
<td>Suspended</td>
<td>Iron</td>
<td> </td>
<td>Suspended</td>
</tr>
<tr>
<td style="text-align: right;">21</td>
<td>PARTN</td>
<td>Nitrogen, particulate</td>
<td>as N</td>
<td>Non-Filterable (Particle)</td>
<td>Total Nitrogen, mixed forms</td>
<td>as N</td>
<td>Non-Filterable (Particle)</td>
</tr>
<tr>
<td style="text-align: right;">22</td>
<td>PARTP</td>
<td>Phosphorus, particulate</td>
<td>as P</td>
<td>Non-Filterable (Particle)</td>
<td>Total Phosphorus, mixed forms</td>
<td>as P</td>
<td>Non-Filterable (Particle)</td>
</tr>
<tr>
<td style="text-align: right;">23</td>
<td>PH</td>
<td>pH, lab</td>
<td> </td>
<td> </td>
<td>pH, lab</td>
<td> </td>
<td> </td>
</tr>
<tr>
<td style="text-align: right;">24</td>
<td>SO4</td>
<td>Sulfate</td>
<td>as SO4</td>
<td>Dissolved</td>
<td>Sulfate</td>
<td>as SO4</td>
<td>Dissolved</td>
</tr>
<tr>
<td style="text-align: right;">25</td>
<td>SR</td>
<td>Spectral ratio</td>
<td> </td>
<td> </td>
<td>Spectral slope ratio</td>
<td> </td>
<td> </td>
</tr>
<tr>
<td style="text-align: right;">26</td>
<td>SRSI</td>
<td>Silica, reactive</td>
<td>as Si</td>
<td> </td>
<td>Silica, reactive</td>
<td>as Si</td>
<td> </td>
</tr>
<tr>
<td style="text-align: right;">27</td>
<td>TDN</td>
<td>Total dissolved nitrogen</td>
<td>as N</td>
<td>Filtered</td>
<td>Total Nitrogen, mixed forms</td>
<td>as N</td>
<td>Filtered</td>
</tr>
<tr>
<td style="text-align: right;">28</td>
<td>TDP</td>
<td>Total dissolved phosphorus</td>
<td>as P</td>
<td>Filtered</td>
<td>Total Phosphorus, mixed forms</td>
<td>as P</td>
<td>Filtered</td>
</tr>
</tbody>
</table>
