---
editor_options: 
  markdown: 
    wrap: 72
---

# OSM Red Squirrel Distribution

Data and code for Brushett et al., 2025 -

<hr>

### GENERAL INFORMATION

**Title:** Predictors of brown bear predation events on livestock in the
Romanian Carpathians

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

**Date of data collection:** 2020 -2024

**Geographic location of data collection:** Oil Sands Region, Alberta,
Canada

**Information about funding sources that supported the collection of the
data:** The data collection was partially funded by the European
Commission LIFE Nature Programme 32 within the project
LIFE08/NAT/RO/000500.The work of MIP and CIJ was supported by a grant 33
of the Romanian Ministry of Education and Research, CNCS- UEFISCDI,
project number PN-34III-P1-1.1-PD-2019-1207, within PNCDI III. MAD and
VDP were supported by the Ohio35 University, Department of Biological
Sciences

### SHARING/ACCESS INFORMATION

**Licenses/restrictions placed on the data:** None

**Link to publications that cite:**
<a href = "https://conbio.onlinelibrary.wiley.com/action/showCitFormats?doi=10.1111%2Fcsp2.12884&mobileUi=0" target = "_blank">[Link
to publication]</a>

**Recommended citation for this dataset:** Brushett et al. (2023), Data
from:

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
    deployed in 2021

-   **OSM_independent_detections_2021_2022_2023.csv;** independent
    detections for all species at each camera site

-   **OSM_landcover_HFI_feature_types.csv;**

-   **OSM_operating_2021_2022_2023.csv;** days of operation for each
    camera trap site

-   **OSM_SBFI2020_metrics.csv;** Satellite-Based Forest Inventory
    variables for all camera trap sites at each buffer size (50 to 5000
    meters)

-   **OSM_simple_config_landscapemetrics.csv;**

-   **OSM_timelapse_2021.csv;**

-   **OSM_timelapse_2022.csv**

-   **OSM_timelapse_2023.csv**

*/processed*

-   **all_models_scales_aic_with_coefficients.csv**
-   **OSM_all_config_covariates_correlation.csv**
-   **OSM_all_config_covariates_correlation_formatted.csv**
-   **OSM_all_covariates_correlation.csv**
-   **OSM_all_covariates_correlation_formatted.csv**
-   **OSM_all_covariates_correlation_new.csv**
-   **OSM_all_covariates_HFI_SBFI_final.csv**
-   **OSM_monthly_detections_2021_2022_2023.csv**
-   **OSM_proportional_monthly_presence_2021_2022_2023.csv**

*Files in scripts folder*

-   **1_Extract_landcover.html**;
-   **1_Extract_landcover.Rmd;**
-   2_Format_covariates.html
-   2_Format_covariates.Rmd
-   3_Explore_covariates.html
-   3_Explore_covariates.Rmd
-   4_Create_response_variables.html
-   4_Create_response_variables.Rmd
-   5_Fit_negative_binomial_models_best_scale.html
-   5_Fit_negative_binomial_models_best_scale.Rmd
-   6_run_simulations.html
-   6_run_simulations.Rmd

### METHODOLOGICAL INFORMATION

**Description of methods used for collection/generation of data:**
Methodological details are provided in the paper
<a href = "Link to publication" target = "_blank">[<https://conbio.onlinelibrary.wiley.com/action/showCitFormats?doi=10.1111%2Fcsp2.12884&mobileUi=0>]</a>

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

### DATA-SPECIFIC INFORMATION FOR: [ [pagube_2008_2016_spatial.csv]{style="color: #7B0F17;"}]

-   **Number of variables:** 24
-   **Number of observations/rows:** 3024

**Variable List:**

-   [**damage**]{style="color: #002747;"}, binary indicator for
    presence/absence of livestock damage caused by brown bears (0 = no
    damage 1 = damage)
-   [**year**]{style="color: #002747;"}, factor describing the year the
    damage was recorded
-   [**month**]{style="color: #002747;"}, numeric notation describing
    the month the damage was recorded (1 = January)
-   [**targetspp**]{style="color: #002747;"}, indicator of the livestock
    type affected
-   [**point_x**]{style="color: #002747;"}, UTM Northing for livestock
    damage
-   [**point_y**]{style="color: #002747;"}, UTM Easting for livestock
    damage
-   [**bear_abund**]{style="color: #002747;"}, relative bear abundance
    estimated by hunters in 2016 and recorded at the game unit level
-   [**landcover_code**]{style="color: #002747;"}, the landcover type in
    2018 as defined by
    <a href = "https://land.copernicus.eu/eagle/files/eagle-related-projects/pt_clc-conversion-to-fao-lccs3_dec2010" target = "_blank">CORINE
    Land Cover Classification system</a>.
-   [**altitude**]{style="color: #002747;"}, the altitude at the
    location recorded in meters.
-   [**human_population**]{style="color: #002747;"}, number of people
    living in administrative units
-   [**dist_to_forest**]{style="color: #002747;"}, distance to nearest
    forest measured in meters
-   [**dist_to_town**]{style="color: #002747;"}, distance to nearest
    human settlement (defined as artificial surface class in CORINE Land
    Cover) measured in meters
-   [**livestock_killed**]{style="color: #002747;"}, number of livestock
    killed per incident
-   [**shannondivindex**]{style="color: #002747;"}, shannon diversity
    index for flora
-   [**prop_arable**]{style="color: #002747;"}, proportion of arable
    land (defined by CORINE Land Cover classification) in 10 km2 area
    around location
-   [**prop_orchards**]{style="color: #002747;"}, proportion of
    orchards/permanent crops (defined by CORINE Land Cover
    classification) in 10 km2 area around location
-   [**prop_pasture**]{style="color: #002747;"}, proportion of pastures
    (defined by CORINE Land Cover classification) in 10 km2 area around
    location
-   [**prop_ag_mosaic**]{style="color: #002747;"}, proportion of
    heterogeneous agricultural areas (defined by CORINE Land Cover
    classification) in 10 km2 area around location
-   [**prop_seminatural**]{style="color: #002747;"}, proportion of
    aseminatural areas (defined by CORINE Land Cover classification) in
    10 km2 area around location
-   [**prop_deciduous**]{style="color: #002747;"}, proportion of
    deciduous forests (defined by CORINE Land Cover classification) in
    10 km2 area around location
-   [**prop_coniferous**]{style="color: #002747;"}, proportion of
    coniferous forests (defined by CORINE Land Cover classification) in
    10 km2 area around location
-   [**prop_mixedforest**]{style="color: #002747;"}, proportion of mixed
    forests (defined by CORINE Land Cover classification) in 10 km2 area
    around location
-   [**prop_grassland**]{style="color: #002747;"}, proportion of
    grasslands (defined by CORINE Land Cover classification) in 10 km2
    area around location
-   [**prop_for_regen**]{style="color: #002747;"}, proportion of
    transitional woodland-shrub (defined by CORINE Land Cover
    classification) in 10 km2 area around location

### DATA-SPECIFIC INFORMATION FOR: [ [cows.csv]{style="color: #7B0F17;"}]

-   **Number of variables:** 34
-   **Number of cases/rows:** 1620

**Variable List:**

-   [**damage**]{style="color: #002747;"}, binary indicator for
    presence/absence of livestock damage caused by brown bears (0 = no
    damage 1 = damage)
-   [**year**]{style="color: #002747;"}, factor describing the year the
    damage was recorded
-   [**month**]{style="color: #002747;"}, numeric notation describing
    the month the damage was recorded (1 = January)
-   [**targetspp**]{style="color: #002747;"}, indicator of the livestock
    type affected
-   [**point_x**]{style="color: #002747;"}, UTM Northing for livestock
    damage
-   [**point_y**]{style="color: #002747;"}, UTM Easting for livestock
    damage
-   [**bear_abund**]{style="color: #002747;"}, relative bear abundance
    estimated by hunters in 2016 and recorded at the game unit level
-   [**landcover_2**]{style="color: #002747;"}, grouped classification
    of CORINE Land Cover variables from landcover_code (see
    brown_bear_predation_data_formatting for specific groupings)
-   [**altitude**]{style="color: #002747;"}, the altitude at the
    location recorded in meters
-   [**human_population**]{style="color: #002747;"}, number of people
    living in administrative units
-   [**dist_to_forest**]{style="color: #002747;"}, distance to nearest
    forest measured in meters
-   [**dist_to_town**]{style="color: #002747;"}, distance to nearest
    human settlement (defined as artificial surface class in CORINE Land
    Cover) measured in meters
-   [**livestock_killed**]{style="color: #002747;"}, number of livestock
    killed per incident
-   [**shannondivindex**]{style="color: #002747;"}, shannon diversity
    index for flora
-   [**prop_arable**]{style="color: #002747;"}, proportion of arable
    land (defined by CORINE Land Cover classification) in 10 km2 area
    around location [**prop_orchards**]{style="color: #002747;"},
    proportion of orchards/permanent crops (defined by CORINE Land Cover
    classification) in 10 km2 area around location
-   [**prop_pasture**]{style="color: #002747;"}, proportion of pastures
    (defined by CORINE Land Cover classification) in 10 km2 area around
    location
-   [**prop_ag_mosaic**]{style="color: #002747;"}, proportion of
    heterogeneous agricultural areas (defined by CORINE Land Cover
    classification) in 10 km2 area around location
-   [**prop_seminatural**]{style="color: #002747;"}, proportion of
    aseminatural areas (defined by CORINE Land Cover classification) in
    10 km2 area around location
-   [**prop_deciduous**]{style="color: #002747;"}, proportion of
    deciduous forests (defined by CORINE Land Cover classification) in
    10 km2 area around location
-   [**prop_coniferous**]{style="color: #002747;"}, proportion of
    coniferous forests (defined by CORINE Land Cover classification) in
    10 km2 area around location
-   [**prop_mixedforest**]{style="color: #002747;"}, proportion of mixed
    forests (defined by CORINE Land Cover classification) in 10 km2 area
    around location
-   [**prop_grassland**]{style="color: #002747;"}, proportion of
    grasslands (defined by CORINE Land Cover classification) in 10 km2
    area around location
-   [**prop_for_regen**]{style="color: #002747;"}, proportion of
    transitional woodland-shrub (defined by CORINE Land Cover
    classification) in 10 km2 area around location
-   [**openhab_10k**]{style="color: #002747;"}, proportion of open
    habitat (landcover_2 grouping) extracted within a 10km2 area around
    each location (using a moving window approach in GIS), scaled and
    centered
-   [**forest_10k**]{style="color: #002747;"}, proportion of forest
    (landcover_2 grouping) extracted within a 10km2 area around each
    location (using a moving window approach in GIS), scaled and
    centered
-   [**urban_10k**]{style="color: #002747;"}, proportion of artificial
    surfaces (landcover_2 grouping) extracted within a 10km2 area around
    each location (using a moving window approach in GIS), scaled and
    centered
-   [**heteroag_10k**]{style="color: #002747;"}, proportion of
    heterogenous agriculture (landcover_2 grouping) extracted within a
    10km2 area around each location (using a moving window approach in
    GIS), scaled and centered
-   [**ag_10k**]{style="color: #002747;"}, proportion of agricultural
    land (landcover_2 grouping) extracted within a 10km2 area around
    each location (using a moving window approach in GIS), scaled and
    centered
-   [**shdi_10k**]{style="color: #002747;"}, shannon diversity index for
    flora calculated for a 10km2 area around each location (using a
    moving window approach in GIS) and based on CORINE Land Cover 2012
    classes, scaled and centered
-   [**s.bear_abund**]{style="color: #002747;"}, scaled and centered
    *bear_abund*
-   [**s.altitude**]{style="color: #002747;"}, scaled and centered
    *altitude*
-   [**s.dist_to_town**]{style="color: #002747;"}, scaled and centered
    *dist_to_town*
-   [**s.dist_to_forest**]{style="color: #002747;"}, scaled and centered
    *dist_to_forest*

### DATA-SPECIFIC INFORMATION FOR: [ [sheep.csv]{style="color: #7B0F17;"}]

-   **Number of variables:** 34
-   **Number of cases/rows:** 844

**Variable List:**

-   [**damage**]{style="color: #002747;"}, binary indicator for
    presence/absence of livestock damage caused by brown bears (0 = no
    damage 1 = damage)
-   [**year**]{style="color: #002747;"}, factor describing the year the
    damage was recorded
-   [**month**]{style="color: #002747;"}, numeric notation describing
    the month the damage was recorded (1 = January)
-   [**targetspp**]{style="color: #002747;"}, indicator of the livestock
    type affected
-   [**point_x**]{style="color: #002747;"}, UTM Northing for livestock
    damage
-   [**point_y**]{style="color: #002747;"}, UTM Easting for livestock
    damage
-   [**bear_abund**]{style="color: #002747;"}, relative bear abundance
    estimated by hunters in 2016 and recorded at the game unit level
-   [**landcover_2**]{style="color: #002747;"}, grouped classification
    of CORINE Land Cover variables from landcover_code (see
    brown_bear_predation_data_formatting for specific groupings)
-   [**altitude**]{style="color: #002747;"}, the altitude at the
    location recorded in meters
-   [**human_population**]{style="color: #002747;"}, number of people
    living in administrative units
-   [**dist_to_forest**]{style="color: #002747;"}, distance to nearest
    forest measured in meters
-   [**dist_to_town**]{style="color: #002747;"}, distance to nearest
    human settlement (defined as artificial surface class in CORINE Land
    Cover) measured in meters
-   [**livestock_killed**]{style="color: #002747;"}, number of livestock
    killed per incident
-   [**shannondivindex**]{style="color: #002747;"}, shannon diversity
    index for flora
-   [**prop_arable**]{style="color: #002747;"}, proportion of arable
    land (defined by CORINE Land Cover classification) in 10 km2 area
    around location [**prop_orchards**]{style="color: #002747;"},
    proportion of orchards/permanent crops (defined by CORINE Land Cover
    classification) in 10 km2 area around location
-   [**prop_pasture**]{style="color: #002747;"}, proportion of pastures
    (defined by CORINE Land Cover classification) in 10 km2 area around
    location
-   [**prop_ag_mosaic**]{style="color: #002747;"}, proportion of
    heterogeneous agricultural areas (defined by CORINE Land Cover
    classification) in 10 km2 area around location
-   [**prop_seminatural**]{style="color: #002747;"}, proportion of
    aseminatural areas (defined by CORINE Land Cover classification) in
    10 km2 area around location
-   [**prop_deciduous**]{style="color: #002747;"}, proportion of
    deciduous forests (defined by CORINE Land Cover classification) in
    10 km2 area around location
-   [**prop_coniferous**]{style="color: #002747;"}, proportion of
    coniferous forests (defined by CORINE Land Cover classification) in
    10 km2 area around location
-   [**prop_mixedforest**]{style="color: #002747;"}, proportion of mixed
    forests (defined by CORINE Land Cover classification) in 10 km2 area
    around location
-   [**prop_grassland**]{style="color: #002747;"}, proportion of
    grasslands (defined by CORINE Land Cover classification) in 10 km2
    area around location
-   [**prop_for_regen**]{style="color: #002747;"}, proportion of
    transitional woodland-shrub (defined by CORINE Land Cover
    classification) in 10 km2 area around location
-   [**openhab_10k**]{style="color: #002747;"}, proportion of open
    habitat (landcover_2 grouping) extracted within a 10km2 area around
    each location (using a moving window approach in GIS), scaled and
    centered
-   [**forest_10k**]{style="color: #002747;"}, proportion of forest
    (landcover_2 grouping) extracted within a 10km2 area around each
    location (using a moving window approach in GIS), scaled and
    centered
-   [**urban_10k**]{style="color: #002747;"}, proportion of artificial
    surfaces (landcover_2 grouping) extracted within a 10km2 area around
    each location (using a moving window approach in GIS), scaled and
    centered
-   [**heteroag_10k**]{style="color: #002747;"}, proportion of
    heterogenous agriculture (landcover_2 grouping) extracted within a
    10km2 area around each location (using a moving window approach in
    GIS), scaled and centered
-   [**ag_10k**]{style="color: #002747;"}, proportion of agricultural
    land (landcover_2 grouping) extracted within a 10km2 area around
    each location (using a moving window approach in GIS), scaled and
    centered
-   [**shdi_10k**]{style="color: #002747;"}, shannon diversity index for
    flora calculated for a 10km2 area around each location (using a
    moving window approach in GIS) and based on CORINE Land Cover 2012
    classes, scaled and centered
-   [**s.bear_abund**]{style="color: #002747;"}, scaled and centered
    *bear_abund*
-   [**s.altitude**]{style="color: #002747;"}, scaled and centered
    *altitude*
-   [**s.dist_to_town**]{style="color: #002747;"}, scaled and centered
    *dist_to_town*
-   [**s.dist_to_forest**]{style="color: #002747;"}, scaled and centered
    *dist_to_forest*

### DATA-SPECIFIC INFORMATION FOR: [ [other.csv]{style="color: #7B0F17;"}]

-   **Number of variables:** 34
-   **Number of cases/rows:** 536

**Variable List:**

-   [**damage**]{style="color: #002747;"}, binary indicator for
    presence/absence of livestock damage caused by brown bears (0 = no
    damage 1 = damage)
-   [**year**]{style="color: #002747;"}, factor describing the year the
    damage was recorded
-   [**month**]{style="color: #002747;"}, numeric notation describing
    the month the damage was recorded (1 = January)
-   [**targetspp**]{style="color: #002747;"}, indicator of the livestock
    type affected
-   [**point_x**]{style="color: #002747;"}, UTM Northing for livestock
    damage
-   [**point_y**]{style="color: #002747;"}, UTM Easting for livestock
    damage
-   [**bear_abund**]{style="color: #002747;"}, relative bear abundance
    estimated by hunters in 2016 and recorded at the game unit level
-   [**landcover_2**]{style="color: #002747;"}, grouped classification
    of CORINE Land Cover variables from landcover_code (see
    brown_bear_predation_data_formatting for specific groupings)
-   [**altitude**]{style="color: #002747;"}, the altitude at the
    location recorded in meters
-   [**human_population**]{style="color: #002747;"}, number of people
    living in administrative units
-   [**dist_to_forest**]{style="color: #002747;"}, distance to nearest
    forest measured in meters
-   [**dist_to_town**]{style="color: #002747;"}, distance to nearest
    human settlement (defined as artificial surface class in CORINE Land
    Cover) measured in meters
-   [**livestock_killed**]{style="color: #002747;"}, number of livestock
    killed per incident
-   [**shannondivindex**]{style="color: #002747;"}, shannon diversity
    index for flora
-   [**prop_arable**]{style="color: #002747;"}, proportion of arable
    land (defined by CORINE Land Cover classification) in 10 km2 area
    around location [**prop_orchards**]{style="color: #002747;"},
    proportion of orchards/permanent crops (defined by CORINE Land Cover
    classification) in 10 km2 area around location
-   [**prop_pasture**]{style="color: #002747;"}, proportion of pastures
    (defined by CORINE Land Cover classification) in 10 km2 area around
    location
-   [**prop_ag_mosaic**]{style="color: #002747;"}, proportion of
    heterogeneous agricultural areas (defined by CORINE Land Cover
    classification) in 10 km2 area around location
-   [**prop_seminatural**]{style="color: #002747;"}, proportion of
    aseminatural areas (defined by CORINE Land Cover classification) in
    10 km2 area around location
-   [**prop_deciduous**]{style="color: #002747;"}, proportion of
    deciduous forests (defined by CORINE Land Cover classification) in
    10 km2 area around location
-   [**prop_coniferous**]{style="color: #002747;"}, proportion of
    coniferous forests (defined by CORINE Land Cover classification) in
    10 km2 area around location
-   [**prop_mixedforest**]{style="color: #002747;"}, proportion of mixed
    forests (defined by CORINE Land Cover classification) in 10 km2 area
    around location
-   [**prop_grassland**]{style="color: #002747;"}, proportion of
    grasslands (defined by CORINE Land Cover classification) in 10 km2
    area around location
-   [**prop_for_regen**]{style="color: #002747;"}, proportion of
    transitional woodland-shrub (defined by CORINE Land Cover
    classification) in 10 km2 area around location
-   [**openhab_10k**]{style="color: #002747;"}, proportion of open
    habitat (landcover_2 grouping) extracted within a 10km2 area around
    each location (using a moving window approach in GIS), scaled and
    centered
-   [**forest_10k**]{style="color: #002747;"}, proportion of forest
    (landcover_2 grouping) extracted within a 10km2 area around each
    location (using a moving window approach in GIS), scaled and
    centered
-   [**urban_10k**]{style="color: #002747;"}, proportion of artificial
    surfaces (landcover_2 grouping) extracted within a 10km2 area around
    each location (using a moving window approach in GIS), scaled and
    centered
-   [**heteroag_10k**]{style="color: #002747;"}, proportion of
    heterogenous agriculture (landcover_2 grouping) extracted within a
    10km2 area around each location (using a moving window approach in
    GIS), scaled and centered
-   [**ag_10k**]{style="color: #002747;"}, proportion of agricultural
    land (landcover_2 grouping) extracted within a 10km2 area around
    each location (using a moving window approach in GIS), scaled and
    centered
-   [**shdi_10k**]{style="color: #002747;"}, shannon diversity index for
    flora calculated for a 10km2 area around each location (using a
    moving window approach in GIS) and based on CORINE Land Cover 2012
    classes, scaled and centered
-   [**s.bear_abund**]{style="color: #002747;"}, scaled and centered
    *bear_abund*
-   [**s.altitude**]{style="color: #002747;"}, scaled and centered
    *altitude*
-   [**s.dist_to_town**]{style="color: #002747;"}, scaled and centered
    *dist_to_town*
-   [**s.dist_to_forest**]{style="color: #002747;"}, scaled and centered
    *dist_to_forest*
