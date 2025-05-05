---
editor_options: 
  markdown: 
    wrap: 72
---

# OSM Red Squirrel Distribution

Data and code for Brushett et al., 2025 - Life of the edge: industrial
footprint and edge effects variably influence the spatial distribution
of a boreal small mammal.

<hr>

### GENERAL INFORMATION

**Title:** Life of the edge: industrial footprint and edge effects
variably influence the spatial distribution of a boreal small mammal

**Author Information (data):**\
Principal Investigator Contact Information\
Name: Jason T. Fisher\
Institution: School of Environmental Studies, University of Victoria,
British Columbia, Canada\
Email: fisherj\@uvic.ca

**Author Information (code):**\
Data Analysis Contact Information\
Name: Aidan Brushett\
Institution: School of Environmental Studies, University of Victoria,
British Columbia, Canada\
Email: [aidanbrushett\@uvic.ca](aidanbrushett@uvic.ca)

Name: Emerald Arthurs\
Institution: School of Environmental Studies, University of Victoria,
British Columbia, Canada\
Email: emeraldarthurs\@uvic.ca

**Date of data collection:** 2021-2023

**Geographic location of data collection:** Oil Sands Region, Alberta,
Canada

**Information about funding sources that supported the collection of the
data:** do we need this?

### SHARING/ACCESS INFORMATION

**Licenses/restrictions placed on the data:** None

**Link to publications that cite:**

**Recommended citation for this dataset:** Brushett et al. (2025), Data
from: Life of the edge: industrial footprint and edge effects variably
influence the spatial distribution of a boreal small mammal

**Recommended citation for this manuscript:**

### DATA & FILE OVERVIEW

**File List:**

*Files in main folder*

-   **OSM_red_squirrel_distribution.Rproj**; R project to run code for
    Brushett et al., 2025
-   **README.html**; a web browser version of this README file
-   **README.md**; a markdown version of this README file that can be
    altered in Rstudio

*Files in data folder*

*/processed*

This folder contains data for the years 2021-2023 that has been cleaned
and formatted using the scripts within the repository.

-   **all_models_scales_aic_with_coefficients.csv - OLD??**
-   **OSM_all_config_covariates_correlation.xlsx;** correlation matrix
    for all configuration variables
-   **OSM_all_config_covariates_correlation_formatted.xlsx;**
    correlation matrix for all configuration metrics, colour coded (dark
    red represents higher correlation)
-   **OSM_all_covariates_correlation.xlsx;** correlation matrix for all
    composition metrics variables
-   **OSM_all_covariates_correlation_formatted.xlsx;** correlation
    matrix for all composition metrics variables, colour coded (dark red
    represents higher correlation)
-   **OSM_all_covariates_correlation_new.xlsx - OLD??**
-   **OSM_all_covariates_HFI_SBFI_final.csv;** all variables from ABMI
    HFI and SBFI
-   **OSM_monthly_detections_2021_2022_2023.csv;** number of detections
    of each species for each month of camera trap deployment for 2021,
    2022, and 2023
-   **OSM_proportional_monthly_presence_2021_2022_2023.csv;**

*/raw*

-   **all_arrays_proportional_presence_monthly_clean.csv**; contains
    monthly presence absence data for all species detected on camera
    traps

-   **OSM_coordinates_2021_2022_2023.csv;** coordinates for all camera
    trap locations (lat, long, WGS 84)

-   **OSM_grouped_config_landscapemetrics.csv;** landscape configuration
    metrics for all camera trap sites at each buffer size (50 to 5000
    meters)

-   **OSM_HFI2021_metrics.csv;** human feature variables for all sites
    at each buffer size (50 to 5000 meters)

-   **OSM_independent_detections_2021_2022_2023.csv;** independent
    detections for all species at each camera site

-   **OSM_landcover_HFI_feature_types.csv; NOT USED?**

-   **OSM_operating_2021_2022_2023.csv;** days of operation for each
    camera trap site

-   **OSM_SBFI2020_metrics.csv;** Satellite-Based Forest Inventory
    variables for all camera trap sites at each buffer size (50 to 5000
    meters)

-   **OSM_simple_config_landscapemetrics.csv;** 'simple' configuration
    metrics — extracted using a raster of human and non-human landcover

-   **OSM_timelapse_2021.csv;** contains cleaned and error-checked image
    data from program Timelapse for all species and LUs sampled in
    2021-2022 (not formatted into independent detections).

-   **OSM_timelapse_2022.csv;** contains cleaned and error-checked image
    data from program Timelapse for all species and LUs sampled in
    2022-2023 (not formatted into independent detections).

-   **OSM_timelapse_2023.csv;** contains cleaned and error-checked image
    data from program Timelapse for all species and LUs sampled in
    2023-2024 (not formatted into independent detections).

*Files in figures folder*

*Files in scripts folder*

-   **1_Extract_landcover.html**;
-   **1_Extract_landcover.Rmd;**
-   **2_Format_covariates.html**
-   **2_Format_covariates.Rmd**
-   **3_Explore_covariates.html**
-   **3_Explore_covariates.Rmd**
-   **4_Create_response_variables.html**
-   **4_Create_response_variables.Rmd**
-   **5_Fit_negative_binomial_models_best_scale.html**
-   **5_Fit_negative_binomial_models_best_scale.Rmd**
-   **6_run_simulations.html**
-   **6_run_simulations.Rmd**

### METHODOLOGICAL INFORMATION

**Description of methods used for collection/generation of data:**
Methodological details are provided in the paper

**Methods for processing the data:** We used generalized linear mixed
effects models with a negative binomial distribution to process the
data. Full details can be found in the paper (link above).

**Instrument- or software-specific information needed to interpret the
data:** We used program R version 4.4.1 with package lme4.

-   Download R
    <a href = "https://cran.r-project.org/bin/windows/" target = "_blank">[Windows
    link]</a>
    <a href = "https://cran.r-project.org/bin/macosx/" target = "_blank">[Mac
    link]</a>
-   Downlad R Studio
    <a href = "https://www.rstudio.com/products/rstudio/" target = "_blank">[link]</a>

**People involved with sample collection, processing, analysis and/or
submission:**

## PROCESSED DATA

### DATA-SPECIFIC INFORMATION FOR [**OSM_all_config_covariates_correlation.xlsx**]

-   **Number of variables:** 10

-   **Number of observations/rows:** 10

-   **NOTE:** there is a sheet for each buffer size (22 sheets)

### DATA-SPECIFIC INFORMATION FOR: [**OSM_all_config_covariates_correlation_formatted.xlsx**]

-   **Number of variables:** 10

-   **Number of cases/rows:** 10

-   **NOTE:** there is a sheet for each buffer size (22 sheets)

### DATA-SPECIFIC INFORMATION FOR: [OSM_all_covariates_correlation.xlsx]

-   **Number of variables:** 35

-   **Number of cases/rows:** 35

-   **NOTE:** there is a sheet for each buffer size (22 sheets)

### DATA-SPECIFIC INFORMATION FOR: [OSM_all_covariates_correlation_formatted.xlsx]

-   **Number of variables:** 35

-   **Number of cases/rows:** 35

-   **NOTE:** there is a sheet for each buffer size (22 sheets)

### DATA-SPECIFIC INFORMATION FOR: [OSM_all_covariates_HFI_SBFI_final.csv]

-   **Number of variables:** 55
-   **Number of cases/rows:** 9461
-   **NOTE:** there is a sheet for each buffer size (22 sheets)

**Variable List:**

-   **array**
-   **site**
-   **array_year**
-   **lat**
-   **long**
-   **easting_12N**
-   **northing_12N**
-   **buffer_dist**
-   **cfi_site**
-   **cfi_site_with_harvest**
-   **cfi_site_with_vegedge**
-   **harvest_0_15**
-   **harvest_gt_15**
-   **harvest_total**
-   **osm_industrial**
-   **pipe_trans**
-   **railways**
-   **roads**
-   **seismic**
-   **seismic_lines**
-   **seismic_lines_3D**
-   **trails**
-   **veg_edges**
-   **wells_active**
-   **well_inactive**
-   **wells_total**
-   **pct_betu_pap**
-   **fire_0_15**
-   **fire_gt_15**
-   **pct_lari_lar**
-   **lc_broadleaf**
-   **lc_conifer**
-   **lc_herbs**
-   **lc_mixedwood**
-   **lc_shrubs**
-   **lc_water**
-   **lc_wetland**
-   **lc_wetland_treed**
-   **pct_pice_gla**
-   **pct_pice_mar**
-   **pct_pinu_ban**
-   **pct_popu_tre**
-   **nonanthro_cai_nm**
-   **nonanthro_ed**
-   **nonanthro_tca**
-   **nonanthro_cai_nm**
-   **landscape_cai_mn**
-   **landscape_ed**
-   **landscape_tca**
-   **nonanthro_cohesion**
-   **landscape_cohesion**
-   **landscape_contag**
-   **landscape_mesh**
-   **landscape_np**
-   **landscape_shei**
-   **landscape_siei**

### DATA-SPECIFIC INFORMATION FOR: [OSM_monthly_detections_2021_2022_2023.csv]

-   **Number of variables:** 7
-   **Number of cases/rows:** 63,935
-   **NOTE:** there is a sheet for each buffer size (22 sheets)

**Variable List:**

-   **array;** a factor with 10 levels describing the landscape unit
    (eg., LU01)
-   **site;** a factor with 430 levels where the first element
    abbreviation describes the landscape unit and the second element
    describes the camera site.
-   **month;** month of the year (1 to 12)
-   **year;** year corresponding to the given month and site
-   **species;** species common name
-   **presence;** whether a species was present (1) or absent (0) in
    that given month
-   **detections;** number of independent detections in the month

## RAW DATA

### DATA-SPECIFIC INFORMATION FOR: [OSM_grouped_config_landscapemetrics.csv]

-   **Number of variables:** 8
-   **Number of cases/rows:** 9461

**Variable List:**

-   **buffer;**
-   **site;** a factor with 430 levels where the first element
    abbreviation describes the landscape unit and the second element
    describes the camera site.
-   **landscape_cohesion**
-   **landscape_contag**
-   **landscape_mesh**
-   **landscape_np**
-   **landscape_shei**
-   **landscape_siei**

### DATA-SPECIFIC INFORMATION FOR: [OSM_HFI2021_metrics.csv]

-   **Number of variables:** 134
-   **Number of cases/rows:** 9461

**Variable List:**

-   **buffer;**
-   **site;** a factor with 430 levels where the first element
    abbreviation describes the landscape unit and the second element
    describes the camera site.
-   buffer_dist
-   **AIRP-RUNWAY;** a numeric variable indicating the proportion of
    airplane runways within the buffer area. Airplane runways are
    defined as, non-vegetated, impermeable surfaces used for motorized
    vehicle or aircraft transportation or access. Specifically, an
    active landing facility for aircraft, usually associated with paved
    and lighted runways, an operating control tower, and services for
    aircraft and passengers.
-   **BORROWPIT-DRY;** a numeric variable indicating the proportion of
    dry borrow pits within the buffer area. Dry borrow pits are defined
    as, excavation outside of the road right-of-way, made solely for the
    purpose of. removing or providing borrowed material for the
    construction of the sub-base for a specific roadway project. It
    includes any other associated infrastructure such as access roads.
    (ALBERTA TRANSPORTAITON; GUIDE TO RECLAIMING BORROW EXCAVATIONS –
    2013 Edition). Specifically, Includes pits dug to build forestry and
    well-site roads. They are usually associated with a road or another
    structure. No presence of water.
-   **BORROWPIT-WET;** a numeric variable indicating the proportion of
    wet borrow pits within the buffer area. Wet borrow pits are defined
    as, excavation outside of the road right-of-way, made solely for the
    purpose of removing or providing borrowed material for the
    construction of the sub-base for a specific roadway project. It
    includes any other associated infrastructure such as access roads.
    (ALBERTA TRANSPORTAITON; GUIDE TO RECLAIMING BORROW EXCAVATIONS –
    2013 Edition). Specifically, includes pits dug to build forestry and
    well-site roads. They are usually associated with a road or another
    structure. Presence of water confirmed by visual interpretation.
-   **BORROWPITS;** a numeric variable indicating the proportion of
    borrow pits within the buffer area. Borrow pits are defined as,
    excavation outside of the road right-of-way, made solely for the
    purpose of removing or providing borrowed material for the
    construction of the sub-base for a specific roadway project. It
    includes any other associated infrastructure such as access roads.
    (ALBERTA TRANSPORTAITON; GUIDE TO RECLAIMING BORROW EXCAVATIONS –
    2013 Edition). Specifically, includes pits dug to build forestry and
    well-site roads. They are usually associated with a road or another
    structure.
-   **CAMP-INDUSTRIAL;** a numeric variable indicating the proportion of
    industrial camps within the buffer area. Industrial camps are
    defined as, human footprint features related to various industrial
    activities. Specifically, buildings used for temporary residence by
    employees on or in close proximity to an industrial activity such as
    mining, forestry, or oil and gas activities.
-   **CAMPGROUND;** a numeric variable indicating the proportion of
    campgrounds within the buffer area. Campgrounds are defined as,
    human footprint related to vegetated facilities and recreation.
    Specifically, disturbed vegetation with frequently changing
    facilities of RVs and tents used for overnight stay. Most often
    consists of several individual clearings surrounded by vegetation
    and gravel or asphalt roads connecting clearings.
-   **CANAL;** a numeric variable indicating the proportion of canals
    within the buffer area. Canals are defined as, a human-made
    watercourse built to convey water for irrigation. An irrigation
    canal is larger than a ditch, with reinforced banks that are usually
    well maintained. A human-made drainage network channels built to
    prepare wetland areas for anthropogenic land use.
-   **CFO;** a numeric variable indicating the proportion of confined
    feeding operations within the buffer area. Confined feeding
    operations are defined as, confined feeding operations and other
    high density livestock features.
-   **CLEARING_UNKNOWN;** a numeric variable indicating the proportion
    of unknown clearings within the buffer area. Unknown clearings are
    defined as, a human-made clearing with unknown purposes and contains
    no visible buildings, fences or equipment.
-   **CLEARING-WELLPAD-UNCONFIRMED;** a numeric variable indicating the
    proportion of unconfirmed clearing well pads within the buffer area.
    Unconfirmed clearing well pads are defined as, human footprint
    features related to various industrial activities. Specifically,
    roughly square in shape clearing, roughly 90-120 meters wide
    (approximately 1 ha). Not confirmed as a well pad by available
    reference sources.
-   **CONVENTIONAL SEISMIC;** a numeric variable indicating the
    proportion of conventional seismic lines within the buffer.
    Conventional seismic lines are defined as, a polygon feature class
    derived from a 3-meter buffer (6 meter total width) of a
    pre-low-impact-seismic centerline.
-   **COUNTRY-RESIDENCE;** a numeric variable indicating the proportion
    of country residence within the buffer area. Country residence is
    defined as, country-residential developments with density of 10 -
    100 buildings per quarter section.
-   **CROP;** a numeric variable indicating the proportion of crop
    within the buffer. Crop is defined as, cultivated cropland or
    cropland planted with annual crop species, including farmlands that
    are in cultivation rotation.
-   **CULTIVATION-ABANDONED;** a numeric variable indicating the
    proportion of abandoned cultivation within the buffer area.
    Abandoned cultivation is defined as, agricultural land that has been
    formally seeded and tilled, but no evidence of present day
    production use. Landscape appears to have a heterogeneous mix of
    vegetation and closely resembles natural cover.
-   **DUGOUT;** a numeric variable indicating the proportion of dugouts
    within the buffer area. Dugouts are defined as, small water storage
    excavations that collect water from runoff from summer rains, a
    surplus of surface water that occurs during snowmelt in the spring
    or from groundwater. (Alberta Agriculture and Rural Development,
    QUALITY FARM DUGOUTS).
-   **FACILITY-OTHER;** a numeric variable indicating the proportion of
    other facilities within the buffer area. Other facilities are
    defined as, human footprint features related to various industrial
    activities. Specifically, industrial facilities characterized by
    large non-residential buildings most often surrounded by concrete
    for parking purposes. The purpose of the facility is not disclosed.
-   **FACILITY-UNKNOWN;** a numeric variable indicating the proportion
    of unknown facilities within the buffer area. Unknown facilities are
    defined as, human footprint features related to various industrial
    activities. Specifically, identifies areas where the reclamation
    liability associated for the disturbance is currently held by
    another industry operator.
-   **GREENSPACE**
-   **HARVEST-AREA-1940**
-   **HARVEST-AREA-1950**
-   **HARVEST-AREA-1960**
-   **HARVEST-AREA-1963**
-   **HARVEST-AREA-1970**
-   **HARVEST-AREA-1971**
-   **HARVEST-AREA-1972**
-   **HARVEST-AREA-1973**
-   **HARVEST-AREA-1975**
-   **HARVEST-AREA-1976**
-   **HARVEST-AREA-1977**
-   **HARVEST-AREA-1978**
-   **HARVEST-AREA-1979**
-   **HARVEST-AREA-1980**
-   **HARVEST-AREA-1984**
-   **HARVEST-AREA-1985**
-   **HARVEST-AREA-1986**
-   **HARVEST-AREA-1987**
-   **HARVEST-AREA-1988**
-   **HARVEST-AREA-1989**
-   **HARVEST-AREA-1990**
-   **HARVEST-AREA-1991**
-   **HARVEST-AREA-1992**
-   **HARVEST-AREA-1993**
-   **HARVEST-AREA-1994**
-   **HARVEST-AREA-1995**
-   **HARVEST-AREA-1996**
-   **HARVEST-AREA-1997**
-   **HARVEST-AREA-1998**
-   **HARVEST-AREA-1999**
-   **HARVEST-AREA-2000**
-   **HARVEST-AREA-2001**
-   **HARVEST-AREA-2002**
-   **HARVEST-AREA-2003**
-   **HARVEST-AREA-2004**
-   **HARVEST-AREA-2005**
-   **HARVEST-AREA-2006**
-   **HARVEST-AREA-2007**
-   **HARVEST-AREA-2008**
-   **HARVEST-AREA-2009**
-   **HARVEST-AREA-2010**
-   **HARVEST-AREA-2011**
-   **HARVEST-AREA-2012**
-   **HARVEST-AREA-2013**
-   **HARVEST-AREA-2014**
-   **HARVEST-AREA-2015**
-   **HARVEST-AREA-2016**
-   **HARVEST-AREA-2017**
-   **HARVEST-AREA-2018**
-   **HARVEST-AREA-2019**
-   **HARVEST-AREA-2020**
-   **HARVEST-AREA-2021**
-   **HARVEST-AREA-WHITE-ZONE**
-   **LAGOON;** a numeric variable indicating the proportion of lagoons
    within the buffer area. Lagoons are defined as, an artificial
    holding or treatment ponds for agricultural or municipal wastewater.
    Human made water and sewage lagoons used for municipal purposes.
-   **LOW-IMPACT-SEISMIC;** a numeric variable indicating the proportion
    of low impact seismic lines within the buffer area. Low impact
    seismic lines are defined as, a polygon feature class derived from a
    1.5-meter buffer (3 meter total width) of a pre-low-impact-seismic
    centerline.
-   **MINES-OILSANDS**
-   **MISC-OIL-GAS-FACILITY;** a numeric variable indicating the
    proportion of misc. oil/gas facilities within the buffer area. Misc.
    oil/gas facilities are defined as, human footprint features related
    to various industrial activities. Specifically, industrial facility
    used for the purpose of oil and gas. BATTERY SITE, COMPRESSOR SITE,
    FLARE STACK, METER STATION SITE, and VALVE SITE.
-   **OIL.GAS.PLANT;** a numeric variable indicating the proportion of
    oil/gas plants within the buffer area. Oil/gas plants are defined
    as, human footprint features related to various industrial
    activities. Specifically, Industrial facility used for oil
    production. REFINERIES, PLANTS, FACTORIES.
-   **OPEN-PIT-MINE;** a numeric variable indicating the proportion of
    open pit mines within the buffer area. Open pit mines are defined
    as, human footprint features directly related to mining activities.
    Specifically, an area of surface disturbance for the purpose of
    mining (with the exception of sand and/or gravel), consistently open
    and/or expanding over multiple years, usually close to lakes or
    rivers.
-   **PIPELINE;** a numeric variable indicating the proportion of
    pipelines within the buffer. Pipelines are defined as, a line of
    underground and overground pipes, of substantial length and
    capacity, used for the conveyance of petrochemicals.
-   **RESERVOIR;** a numeric variable indicating the proportion of
    reservoirs within the buffer area. Reservoirs are defined as, an
    artificial lake or storage pond resulting from human-made dam. A
    body of water created by excavation or the man-made damming of a
    river or stream.
-   **RESIDENCE_CLEARING;** a numeric variable indicating the proportion
    of residence clearing within the buffer area. Residence clearing is
    defined as, areas cleared for building developments that do not yet
    have any buildings.
-   **RIS-CAMP-INDUSTRIAL**
-   **RIS-CLEARING-UNKNOWN**
-   **RIS-DRAINAGE**
-   **RIS-FACILITY-OPERATIONS**
-   **RIS-FACILITY-UNKNOWN**
-   **RIS-MINES-OILSANDS**
-   **RIS-OILSANDS-RMS**
-   **RIS-OVERBURDEN-DUMP**
-   **RIS-RECLAIMED-PERMANENT**
-   **RIS-RECLAIMED-TEMP**
-   **RIS-ROAD**
-   **RIS-SOIL-REPLACED**
-   **RIS-SOIL-SALVAGED**
-   **RIS-TAILING-POND**
-   **RIS-TRANSMISSION-LINE**
-   **RIS-UTILITIES**
-   **RIS-WINDROW**
-   **RLWY-SGL-TRACK**
-   **ROAD-GRAVEL-1L**
-   **ROAD-GRAVEL-2L**
-   **ROAD-PAVED-DIV**
-   **ROAD-PAVED-UNDIV-1L**
-   **ROAD-PAVED-UNDIV-2L**
-   **ROAD-UNCLASSIFIED**
-   **ROAD-UNIMPROVED**
-   **ROAD-WINTER**
-   **ROUGH_PASTURE**
-   **RUNWAY**
-   **RURAL-RESIDENCE**
-   **SUMP**
-   **SURROUNDING-VEG**
-   **TAILING-POND**
-   **TAME_PASTURE**
-   **TRAIL**
-   **TRANSMISSION-LINE**
-   **TRUCK-TRAIL**
-   **URBAN-INDUSTRIAL**
-   **URBAN-RESIDENCE**
-   **VEGETATED-EDGE-RAILWAYS**
-   **VEGETATED-EDGE-ROADS**
-   **WELL-ABAND**
-   **WELL-BITUMEN**
-   **WELL-CASED**
-   **WELL-GAS**
-   **WELL-OIL**
-   **WELL-OTHER**
-   **WELL-UNKNOWN**
-   **WELL_CLEARED_NOT_CONFIRMED**
-   **WELL_CLEARED_NOT_DRILLED**

### DATA-SPECIFIC INFORMATION FOR: [OSM_independent_detections_2021_2022_2023.csv]

-   **Number of variables:** 8
-   **Number of cases/rows:** 34,540

**Variable List:**

-   **array;** a factor with 10 levels describing the landscape unit
    (eg., LU01)
-   **camera;**
-   **site;** a factor with 430 levels where the first element
    abbreviation describes the landscape unit and the second element
    describes the camera site.
-   **species;** species present in the independent event
-   **event_start;** independent event start date/time, format:
    YYYY-MM-DD HH:MM:SS
-   **event_end;** independent event end date/time, format: YYYY-MM-DD
    HH:MM:SS
-   **year:** year in which the independent event was captured
-   **month;** month in which the independent event was captured (1 to
    12) 

### DATA-SPECIFIC INFORMATION FOR: [OSM_landcover_HFI_feature_types.csv]

-   **Number of variables:** 9
-   **Number of cases/rows:** 106

**Variable List:**

### DATA-SPECIFIC INFORMATION FOR: [OSM_operating_2021_2022_2023.csv]

-   **Number of variables:** 4
-   **Number of cases/rows:** 149,275

**Variable List:**

-   **array;** a factor with 10 levels describing the landscape unit
    (eg., LU01)
-   **camera;** number of the camera site
-   **site;** a factor with 430 levels where the first element
    abbreviation describes the landscape unit and the second element
    describes the camera site.
-   **date;** day that the camera was active (a new row for each day),
    format: YYY-MM-DD
