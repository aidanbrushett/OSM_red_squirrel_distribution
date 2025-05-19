---
editor_options: 
  markdown: 
    wrap: 72
---

# OSM Red Squirrel Distribution

Data and code for Brushett et al., 2025 - Life of the edge: industrial
footprint and edge effects variably influence the spatial distribution
of a boreal small mammal.

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

**Dates of data collection:** 2021-2023

**Geographic location of data collection:** Oil Sands Region, Alberta,
Canada

**Information about funding sources that supported the collection of the
data:** do we need this?

### SHARING/ACCESS INFORMATION

**Licenses/restrictions placed on the data:** None

**Link to publications that cite:**

**Recommended citation for this dataset:** Brushett, A., Arthurs, E., &
Fisher, J. (2025). Life of the edge: industrial footprint and edge
effects variably influence the spatial distribution of a boreal small
mammal [dataset].
<https://github.com/aidanbrushett/OSM_red_squirrel_distribution>

**Recommended citation for this manuscript:** Brushett, A., Arthurs, E.,
& Fisher, J. (2025). Life of the edge: industrial footprint and edge
effects variably influence the spatial distribution of a boreal small
mammal. *Add journal information once published.*

### DATA & FILE OVERVIEW

**File List:**

[*Files in main folder:*]{.underline}

-   **OSM_red_squirrel_distribution.Rproj**; R project to run code for
    Brushett et al., 2025
-   **README.html**; a web browser version of this README file
-   **README.md**; a markdown version of this README file that can be
    altered in RStudio, VSCode, or any other code editor.

[*Files in data folder*]{.underline}

*/processed*

This folder contains data for the years 2021-2023 that has been cleaned
and formatted using the scripts within the repository.

-   **OSM_all_covariates_correlation_formatted.xlsx;** correlation
    matrix for all candidate landscape metrics (including composition
    *and* configuration variables) at all possible spatial scales
    (50-5000 m; one scale per tab). Correlation values are colour coded
    (dark red represents higher correlation).
-   **OSM_all_covariates_HFI_SBFI_final.csv;** all landscape metrics
    extracted for camera trap sites at all possible spatial scales
    (50-5000 m). Includes coordinates, sample year, and all
    configuration and composition metrics derived from the Alberta
    Biodiersity Monitoring Institute's *2021 Human Footprint Inventory
    (HFI)* and Wulder's et al. (2024) *2020 Satellite Based Forest
    Inventory (SBFI).*
-   **OSM_monthly_detections_2021_2022_2023.csv;** number of detections
    of each species for each month of camera trap deployment for 2021,
    2022, and 2023.

*/raw*

-   **OSM_coordinates_2021_2022_2023.csv;** coordinates for all camera
    trap locations (lat, long, WGS 84)

-   **OSM_grouped_config_landscapemetrics.csv;** landscape-scale
    configuration metrics for all camera trap sites at each buffer size
    (50 to 5000 meters). These were extracted using a rasterized
    representation of the landscape with all original land cover
    polygons represented. This is an output from script 1.

-   **OSM_HFI2021_metrics.csv;** human feature variables for all sites
    at each buffer size (50 to 5000 meters) derived from the Alberta
    Biodiersity Monitoring Institute's *2021 Human Footprint Inventory
    (HFI)*. This is an output from script 1.

-   **OSM_independent_detections_2021_2022_2023.csv;** independent
    detections for all species at each camera site.

-   **OSM_operating_2021_2022_2023.csv;** days of operation for each
    camera trap site

-   **OSM_SBFI2020_metrics.csv;** Satellite-Based Forest Inventory
    variables for all camera trap sites at each buffer size (50 to 5000
    meters) derived from Wulder's et al. (2024) *2020 Satellite Based
    Forest Inventory (SBFI).* This is an output from script 1.

-   **OSM_simple_config_landscapemetrics.csv;** 'simple' class-specific
    configuration metrics for all camera trap sites at each buffer size
    (50 to 5000 meters). These were extracted using a rasterized
    representation of the landscape with simplified classes representing
    anthropogenic footprint (*anthro*), remaining 'natural' habitat
    matrix (*nonanthro*), and water. This is an output from script 1.

-   **OSM_timelapse_2021.csv;** contains cleaned and error-checked image
    data from program Timelapse for all species and LUs sampled in
    2021-2022 (not formatted into independent detections).

-   **OSM_timelapse_2022.csv;** contains cleaned and error-checked image
    data from program Timelapse for all species and LUs sampled in
    2022-2023 (not formatted into independent detections).

-   **OSM_timelapse_2023.csv;** contains cleaned and error-checked image
    data from program Timelapse for all species and LUs sampled in
    2023-2024 (not formatted into independent detections).

[*Files in scripts folder:*]{.underline}

All scripts in this folder are accompanied by the knitted .*HTML* and
*.PDF* outputs of the R Markdown files. The HTML files are the most
readable format and we encourage readers to check these when looking at
scripts for interest.

-   **1_Extract_landcover.Rmd;** script to extract the landscape metrics
    for all sites in the study area.
-   **2_Format_covariates.Rmd;** script to append, combine, and rename
    the landscape metrics for all sites in the study area that were
    extracted in the previous script.
-   **3_Explore_covariates.Rmd;** script to conduct exploratory analysis
    of all potential landscape covariates in the dataset prior to
    modelling.
-   **4_Create_response_variables.Rmd;** script to create and explore
    potential response variables describing the spatial distribution of
    red squirrels in the study area.
-   **5_Fit_negative_binomial_models_best_scale.Rmd;** script to fit,
    evaluate, and visualize all models of landscape structure and its
    influence on the spatial distribution of red squirrels in the study
    area.
-   **6_run_simulations.Rmd;** script to fit models to simulated data
    and evaluate the predictive accuracy of the red squirrel models.

[*Files in figures folder:*]{.underline}

This folder contains various plots generated in the scripts of this
repository for the purposes of data visualization.

-   **allarrays_monthly_detections.png;** plot depicting the number of
    detections per month, grouped by landscape unit; generated in the
    4_Create_response variable.rmd script

-   **odds_ratio_top_model_second_model.png;** plot depiciting the
    standardized odds ratios for each variable in top models; generated
    in the 5_Fit_negative_binomial_models_best_scale.rmd script

-   **redsquirrel_neg_binomial_submodel_scale_modelweight.png;** plot
    depicting the AICc weight of top models for each covariate subset
    across all buffer sizes; generated in the
    5_Fit_negative_binomial_models_best_scale.rmd script

-   **top_model_all_effects.png;** plot depicting the conditional
    effects of each variable in the top model; generated in the
    5_Fit_negative_binomial_models_best_scale.rmd script

-   **top_model_diagnostics.png;** plot depicting diagnostic plots for
    checking model assumptions; generated in the
    5_Fit_negative_binomial_models_best_scale.rmd script

-   **top_model_simulations_coefficient_density_gaussian_sampler.png;**
    plot depicting the results of the simulations using the Gaussian
    distribution sampler; generated in the 6_run_simulations.rmd script

-   **top_model_simulations_coefficient_density_reduced_sample_size.png;**
    plot depicting the results of the simulations using the uniform
    distribution sampler and a reduced sample size; generated in the
    6_run_simulations.rmd script

-   **top_model_simulations_coefficient_density_uniform_sampler.png;**
    plot depicting the results of the simulations using the uniform
    distribution sampler; generated in the 6_run_simulations.rmd script

[*Files in tables folder:*]{.underline}

This folder contains summary tables used for the production of the final
manuscript. They are not used as data sources.

-   **OSM_all_covariates_formatted_names.csv;** relational table
    describing landscape covariates as named in the source data
    (*Covariate*) and their respective formatted names used for figures
    and tables in the manuscript (*PrettyName*).

-   **OSM_all_covariates_summary_formatted.xlsx**; summary table
    describing covariates (*Covariate)*, their final modeled spatial
    scale in candidate models, their median and 5%/95% quantiles, and
    their brief description (*Description)*

-   **OSM_final_dataset_high_correlation.xlsx;** a pairwise table of
    Spearman's r for variables with correlation \>0.6. Used to populate
    the Supporting Information document.

-   **OSM_model_selection_summary_formatted.xlsx;** a table of model
    selection results from the candidate model set. Models are ordered
    by their AICc rank. Includes main hypothesis corresponding to the
    model, model covariates, and model selection metrics (*degrees of
    freedom, AICc, delta AICc, and model weight*).

-   **OSM_top_model_summary_formatted.xlsx;** Beta coefficient
    estimates, standard errors, and p values for metrics included in the
    top-ranked model from the model selection table. Standard deviation
    of the random intercept estimates are also included.

-   **OSM_second_model_summary.xlsx;** Beta coefficient estimates,
    standard errors, and p values for metrics included in the
    second-ranked model from the model selection table. Standard
    deviation of the random intercept estimates are also included.

### METHODOLOGICAL INFORMATION

**Description of methods used for collection/generation of data:**
Methodological details are provided in the manuscript.

**Methods for processing the data:** We used generalized linear mixed
effects models with a negative binomial distribution to process the
data. Full details can be found in the paper (link above).

**Instrument- or software-specific information needed to interpret the
data:** We used program R version 4.4.1 with package glmmTMB.

-   Download R
    <a href = "https://cran.r-project.org/bin/windows/" target = "_blank">[Windows
    link]</a>
    <a href = "https://cran.r-project.org/bin/macosx/" target = "_blank">[Mac
    link]</a>
-   Downlad R Studio
    <a href = "https://www.rstudio.com/products/rstudio/" target = "_blank">[link]</a>

**People involved with sample collection, processing, analysis and/or
submission:**

Aidan Brushett and Emerald Arthurs conceived the study, designed the
methodology, analyzed the data, and wrote the first draft of the
manuscript; Aidan Brushett, Emerald Arthurs, and Jason Fisher collected
the data; Jason Fisher oversaw the experimental design; All authors
contributed meaningfully to the final draft of the manuscript and gave
final approval for publication. Field data were collected by Millicent
Gaston, Rebecca Smith, Andrew Barnas, MacGregor Aubertin-Young, Laura
Eliuk, Sandra Frey, Nicole Boucher, Shay Marks, Emerald Arthurs, Aidan
Brushett, Madison Carlson, Megan Braun, Jamie Clarke, and Marissa Dyck.

## PROCESSED DATA

### DATA-SPECIFIC INFORMATION FOR: [OSM_all_covariates_correlation_formatted.xlsx]

-   **Number of variables:** 35

-   **Number of cases/rows:** 35

-   **NOTE:** there is a sheet for each buffer size (22 sheets for
    buffers from 50 m to 5000 m). Covariate names correspond to those in
    *OSM_all_covariates_HFI_SBFI_final.csv* that were also considered in
    candidate models. All covariates are described below:

### DATA-SPECIFIC INFORMATION FOR: [OSM_all_covariates_HFI_SBFI_final.csv]

-   **Number of variables:** 55
-   **Number of cases/rows:** 9461
-   **NOTE:** there is a sheet for each buffer size (22 sheets
    representing 50 m to 5000 m)

**Variable List:**

-   **array;** a factor with 10 levels describing the landscape unit
    (eg., LU01)
-   **site;** a factor with 430 levels where the first element
    abbreviation describes the landscape unit and the second element
    describes the camera site.
-   **array_year;** a factor with 3 levels that describes the year the
    camera was deployed
-   **lat;** latitude of the camera location in decimal degrees (WGS84)
-   **long;** longitude of the camera location in decimal degrees
    (WGS84)
-   **easting_12N;** easting coordinate of the camera site(NAD 83 UTM
    Zone 12N)
-   **northing_12N;** northing coordinate of the camera site(NAD 83 UTM
    Zone 12N)
-   **buffer_dist;** a numeric measurement in meters ranging from 50 -
    5000, of the buffer radius around the camera for which the
    proportion of all variables were calculated.
-   **harvest_0\_15;** a numeric variable indicating the proportion of
    the buffer area comprised of
-   of harvest areas harvested within the past 15 years.
-   **harvest_gt_15;** a numeric variable indicating the proportion of
    the buffer area comprised of of harvest areas harvested over 15
    years ago.
-   **harvest_total;** a numeric variable indicating the proportion of
    all harvest areas within the buffer area.
-   **osm_industrial;** a numeric measurement representing the
    proportion of various industrial features and clearings within the
    buffer. This includes, borrowpits (i.e., Borrowpit-dry,
    Borrowpit-wet, Borrowpits, Ris-borrowpits, Dugout, Lagoon, and
    Sump), clearings (i.e., Clearing-unknown,
    Clearing-wellpad-unconfirmed, Ris-clearing, Ris-clearing-unknown,
    and Runway), facilities (i.e., Camp-industrial, Facility-other,
    Facility-unknown, Mill, Misc-oil-gas-facility, Oil-gas-plant,
    Ris-camp-industrial, Ris-facility-operations, Ris-facility-unknown,
    Ris-plant, Ris-tank-farm, Ris-utilities, and Urban-industrial), and
    mines (i.e., Grvl-sand-pit, Mines-oilsands, Mines-pitlake,
    Open-pit-mine, Peat, Ris-drainage, Ris-mines-oilsands,
    Ris-oilsands-rms, Ris-overburden-dump, Ris-reclaim-ready,
    Ris-soil-salvaged, Ris-tailing-pond, Ris-waste, and Tailing-pond).
-   **pipe_trans;** a numeric measurement representing the proportion of
    pipelines and transmission lines within the buffer.
-   **railways;** a numeric variable indicating the proportion of single
    track railways within the buffer area. Single track railways are
    defined as, hard, steel rail lines designed for train use.
    Specifically, a road or track for trains, consisting of parallel
    steel rails, supported on wooden crossbeams. The single track
    consists of one parallel sets of tracks.
-   **roads**; a numeric measurement representing the proportion of
    roads within the buffer. Roads are defined as, non-vegetated,
    impermeable surfaces used for motorized vehicle or aircraft
    transportation or access and includes, Airp-runway,
    Interchange-ramp, Ris-airp-runway, Ris-road, Road-gravel-1L,
    Road-gravel-2L, Road-paved-1L, Road-paved-2L, Road-paved-3L,
    Road-paved-4L, Road-paved-5L, Road-paved-6L, Road-paved-7L,
    Road-paved-div, Road-paved-undiv-1L, Road-paved-undiv-2L,
    Road-unclassified, Road-unimproved, Road-unpaved-1L,
    Road-unpaved-2L, Road-winter, and Transfer station.
-   **seismic;** a numeric measurement representing the proportion of
    seismic lines and 3D seismic lines within the buffer.
-   **seismic_lines;** a numeric measurement representing the proportion
    of seismic lines within the buffer. Seismic lines are defined as,
    cleared corridors created during hydrocarbon exploration with a
    3-meter buffer (6-meter total width), and were not grouped with any
    other variables.
-   **seismic_lines_3D;** a numeric measurement representing the
    proportion of 3D seismic lines (also called low-impact seismic
    lines) within the buffer. 3D seismic lines are defined as, cleared
    corridors created during hydrocarbon exploration with a 1.5-meter
    buffer (3-meter total width), and were not grouped with any other
    variables.
-   **trails;** a numeric measurement representing the proportion of
    trails within the buffer. Trails are defined as, cleared corridors
    surfaced with dirt or low vegetation for human/vehicle access, and
    include Trail, and Truck-trail.
-   **veg_edges;** a numeric measurement representing the proportion of
    vegetated edges within the buffer. Vegetated edges are defined as,
    disturbed vegetation alongside road edges, railway edges including
    ditches, and other industrial features, and include
    Vegetated-edge-railways, Vegetated-edge-roads, and Surrounding-veg.
-   **wells_active;** a numeric measurement representing the proportion
    of active wells within the buffer. Active wells are defined as,
    ground cleared for an oil/gas well pad where at least one well is
    currently active include, Well-bitumen, Well-cased,
    Well-cleared-not-confirmed, Well-cleared-not-drilled, Well-gas,
    Well-oil, Well-other, and Well-unknown.
-   **well_inactive;** a numeric measurement representing the proportion
    of inactive wells within the buffer. Inactive ells are defined as,
    ground cleared for an oil/gas well pad, where the well is currently
    abandoned.
-   **wells_total;** a numeric measurement representing the proportion
    of wells within the buffer. Wells are defined as, ground cleared for
    an oil/gas well pad, and include Well-abandoned, Well-bitumen,
    Well-cased, Well-cleared-not-confirmed, Well-cleared-not-drilled,
    Well-gas, Well-oil, Well-other, and Well-unknown.
-   **pct_betu_pap;** a numeric variable indicating the proportion of
    Betula papyrifera (White birch) within the buffer area.
-   **fire_0\_15;** a numeric variable indicating the proportion of
    burned area up to 15 years old within the buffer area.
-   **fire_gt_15;** a numeric variable indicating the proportion of
    burned area over 15 years ago within the buffer area.
-   **pct_lari_lar;** a numeric variable indicating the proportion of
    Larix laricina (Tamarack) within the buffer area.
-   **lc_broadleaf;** a numeric variable indicating the proportion of
    broadleaf forest within the buffer area.
-   **lc_conifer;** a numeric variable indicating the proportion of
    conifer forest within the buffer area.
-   l**c_herbs;** a numeric variable indicating the proportion of herb
    within the buffer area.
-   **lc_mixedwood;** a numeric variable indicating the proportion of
    mixedwood forest within the buffer area.
-   **lc_shrubs;** a numeric variable indicating the proportion of
    shrubs within the buffer area.
-   **lc_water;** a numeric variable indicating the proportion of water
    within the buffer area.
-   **lc_wetland;** a numeric variable indicating the proportion of
    wetland within the buffer area.
-   **lc_wetland_treed;** a numeric variable indicating the proportion
    of treed wetland within the buffer area.
-   **pct_pice_gla;** a numeric variable indicating the proportion of
    Larix laricina (White spruce) within the buffer area.
-   **pct_pice_mar;** a numeric variable indicating the proportion of
    Picea mariana (Black spruce) within the buffer area.
-   **pct_pinu_ban;** a numeric variable indicating the proportion of
    Pinus banksaina (Jack pine) within the buffer area.
-   **pct_popu_tre;** a numeric variable indicating the proportion of
    Populus tremuloides (Trembling aspen) within the buffer area.
-   **nonanthro_cai_mn;** a numeric variable indicating the mean of the
    core area index of natural habitat relative to any anthropogenic
    disturbance features - a good proxy for disturbance relief within
    the buffer area. Described at:
    [https://r-spatialecology.github.io/landscapemetrics/reference/lsm_c\_cai_mn.html](https://r-spatialecology.github.io/landscapemetrics/reference/lsm_l_tca.html){style="font-size: 11pt;"}
-   **nonanthro_ed;** a numeric variable indicating the edge density of
    natural habitat, representing the density of edges created by
    borders with any anthropogenic disturbances in meters per hectare
    (m/Ha). Described at:
    [https://r-spatialecology.github.io/landscapemetrics/reference/lsm_c\_ed.html](https://r-spatialecology.github.io/landscapemetrics/reference/lsm_l_tca.html){style="font-size: 11pt;"}
-   **nonanthro_tca;** a numeric variable indicating the total core area
    of natural habitat relative to edges created by any anthropogenic
    disturbances, representing the amount of natural habitat that is \>
    50 meters from the edge within the buffer area in square meters.
    Described at:
    [https://r-spatialecology.github.io/landscapemetrics/reference/lsm_c\_tca.html](https://r-spatialecology.github.io/landscapemetrics/reference/lsm_l_tca.html)
-   **landscape_cai_mn;** a numeric variable indicating the mean of the
    core area index of all patches within the buffer area. Unitless.
    Described at:
    [https://r-spatialecology.github.io/landscapemetrics/reference/lsm_l\_cai_mn.html](https://r-spatialecology.github.io/landscapemetrics/reference/lsm_l_tca.html)
-   **landscape_ed;** a numeric variable indicating the density of edges
    between any land cover types within the buffer area, measured in
    m/Ha. Described at:
    [https://r-spatialecology.github.io/landscapemetrics/reference/lsm_l\_ed.html](https://r-spatialecology.github.io/landscapemetrics/reference/lsm_l_tca.html)
-   **landscape_tca;** a numeric variable indicating the total core
    area, representing the amount of the patch that is \> 50 meters from
    the edge within the buffer area. Measured in square meters.
    Described at:
    <https://r-spatialecology.github.io/landscapemetrics/reference/lsm_l_tca.html>
-   **nonanthro_cohesion;** a numeric variable indicating natural
    habitat cohesion, representing the chances that two points of a
    class are connected within the buffer area. Described at:
    [https://r-spatialecology.github.io/landscapemetrics/reference/lsm_c\_cohesion.html](https://r-spatialecology.github.io/landscapemetrics/reference/lsm_l_cohesion.html)
-   **landscape_cohesion;** a numeric variable indicating the patch
    cohesion index representing the chances that two points are
    connected within the buffer area. Described at:
    <https://r-spatialecology.github.io/landscapemetrics/reference/lsm_l_cohesion.html>
-   **landscape_contag;** a numeric variable indicating the contagion,
    described at:
    <https://r-spatialecology.github.io/landscapemetrics/reference/lsm_l_contag.html>
-   **landscape_mesh;** a numeric variable indicating the mesh index,
    described at:
    <https://r-spatialecology.github.io/landscapemetrics/reference/lsm_c_mesh.html>
-   **landscape_np;** a numeric variable indicating the total number of
    patches, representing a measure of patch size within the buffer
    area. Described at:
    [https://r-spatialecology.github.io/landscapemetrics/reference/lsm_l\_np.html](https://r-spatialecology.github.io/landscapemetrics/reference/lsm_l_tca.html){style="font-size: 11pt;"}
-   **landscape_shei;** a numeric variable indicating the Shannon
    evenness index within the buffer area. Described at:
    <https://r-spatialecology.github.io/landscapemetrics/reference/lsm_l_shei.html>
-   **landscape_siei;** a numeric variable indicating the Simpson
    evenness index within the buffer area. Described at:
    [https://r-spatialecology.github.io/landscapemetrics/reference/lsm_l\_siei.html](https://r-spatialecology.github.io/landscapemetrics/reference/lsm_l_shei.html)

### DATA-SPECIFIC INFORMATION FOR: [OSM_monthly_detections_2021_2022_2023.csv]

-   **Number of variables:** 7
-   **Number of cases/rows:** 63,935
-   **NOTE:** there is a sheet for each buffer size (22 sheets)

**Variable List:**

-   **array;** a factor with 10 levels describing the landscape unit
    (e.g., LU01).
-   **site;** a factor with 430 levels where the first element
    abbreviation describes the landscape unit and the second element
    describes the camera site.
-   **month;** numeric, month of the year (1 to 12).
-   **year;** factor, year corresponding to observation in a the given
    month and site
-   **species;** species common name for twelve focal species in the Oil
    Sands Region (not just squirrels!!).
-   **presence;** whether a species was present (1) or absent (0) in
    that given month.
-   **detections;** number of independent detections of a species in a
    given month at a given camera site.

## RAW DATA

### DATA-SPECIFIC INFORMATION FOR: [OSM_coordinates_2021_2022_2023.csv]

-   **Number of variables:** 4
-   **Number of cases/rows:** 433
-   **NOTE:** Three sites had insufficient data to be included in
    models, hence the discrepancy in the number of sites between this
    file and the *processed/* data files

**Variable list:**

-   **array**, factor describing the landscape unit of a camera (i.e.
    LU09, LU16, LU14, or LU22).

-   **site**, factor where the first element abbreviation describes the
    landscape unit and the second element describes the camera site.

-   **lat**, site latitude in decimal degrees (WGS84)

-   **long**, site longitude in decimal degrees (WGS84)

### DATA-SPECIFIC INFORMATION FOR: [OSM_grouped_config_landscapemetrics.csv]

-   **Number of variables:** 8
-   **Number of cases/rows:** 9461
-   **NOTE:** An intermediate file wherein all variables used in final
    analysis are decribed under
    "processed/OSM_all_covariates_HFI_SBFI_final.csv"

### DATA-SPECIFIC INFORMATION FOR: [OSM_HFI2021_metrics.csv]

-   **Number of variables:** 134
-   **Number of cases/rows:** 9461

**Variable List:**

-   **buffer;** a numeric measurement in meters ranging from 50 - 5000,
    of the buffer radius around the camera for which the proportion of
    associated human factors variables were calculated.
-   **site;** a factor with 430 levels where the first element
    abbreviation describes the landscape unit and the second element
    describes the camera site.
-   **buffer_dist;** the radius of the circular buffer (in meters)
    around each camera site for which variables were extracted
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
    (ALBERTA TRANSPORTAITON; GUIDE TO RECLAIMING BORROW EXCAVATIONS --
    2013 Edition). Specifically, Includes pits dug to build forestry and
    well-site roads. They are usually associated with a road or another
    structure. No presence of water.
-   **BORROWPIT-WET;** a numeric variable indicating the proportion of
    wet borrow pits within the buffer area. Wet borrow pits are defined
    as, excavation outside of the road right-of-way, made solely for the
    purpose of removing or providing borrowed material for the
    construction of the sub-base for a specific roadway project. It
    includes any other associated infrastructure such as access roads.
    (ALBERTA TRANSPORTAITON; GUIDE TO RECLAIMING BORROW EXCAVATIONS --
    2013 Edition). Specifically, includes pits dug to build forestry and
    well-site roads. They are usually associated with a road or another
    structure. Presence of water confirmed by visual interpretation.
-   **BORROWPITS;** a numeric variable indicating the proportion of
    borrow pits within the buffer area. Borrow pits are defined as,
    excavation outside of the road right-of-way, made solely for the
    purpose of removing or providing borrowed material for the
    construction of the sub-base for a specific roadway project. It
    includes any other associated infrastructure such as access roads.
    (ALBERTA TRANSPORTAITON; GUIDE TO RECLAIMING BORROW EXCAVATIONS --
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
-   **GREENSPACE;** a numeric variable indicating the proportion of
    greenspace within the buffer area. Green space is defined as,
    greenspace used for recreation within a residential area including
    parks, schools, school yards and sports fields.
-   **HARVEST-AREA-1940;** a numeric variable indicating the proportion
    of harvest area from 1940 or earlier in the buffer area. Harvest
    area is defined as, areas in Alberta's forested Green Zone where
    forestry operations have occured (clear-cut, selective harvest,
    salvage logging, etc.).
-   **HARVEST-AREA-1950;** a numeric variable indicating the proportion
    of harvest area from 1941 to 1950 in the buffer area.
-   **HARVEST-AREA-1960;** a numeric variable indicating the proportion
    of harvest area from 1951 to 1960 in the buffer area.
-   **HARVEST-AREA-1963;** a numeric variable indicating the proportion
    of harvest area from 1961 to 1963 in the buffer area.
-   **HARVEST-AREA-1970;** a numeric variable indicating the proportion
    of harvest area in the year 1970 in the buffer area.
-   **HARVEST-AREA-1971;** a numeric variable indicating the proportion
    of harvest area in the stated year (1971) in the buffer area. All
    columns below follow the same convention:
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
-   **HARVEST-AREA-WHITE-ZONE;** a numeric variable indicating the
    proportion of harvest area white zone within the buffer. Harvest
    area white zone is defined as, areas where forestry operations have
    occurred (clear-cut, selective harvest, salvage logging, etc.).
    specifically, areas in Alberta's unforested White Zone where woody
    vegetation (i.e. shrub, trees, etc..) have been removed and the
    purpose of the clearing has not yet been determined.
-   **LAGOON;** a numeric variable indicating the proportion of lagoons
    within the buffer area. Lagoons are defined as, an artificial
    holding or treatment ponds for agricultural or municipal wastewater.
    Human made water and sewage lagoons used for municipal purposes.
-   **LOW-IMPACT-SEISMIC;** a numeric variable indicating the proportion
    of low impact seismic lines within the buffer area. Low impact
    seismic lines are defined as, a polygon feature class derived from a
    1.5-meter buffer (3 meter total width) of a pre-low-impact-seismic
    centerline.
-   **MINES-OILSANDS;** a numeric variable indicating the proportion of
    oil sands mines within the buffer area. Oil sands mines are defined
    as, heavy industry use with bare and/or vegetated ground and low
    human density for the purpose of oil sands mining.
-   **MISC-OIL-GAS-FACILITY;** a numeric variable indicating the
    proportion of misc. oil/gas facilities within the buffer area. Misc.
    oil/gas facilities are defined as, human footprint features related
    to various industrial activities. Specifically, industrial facility
    used for the purpose of oil and gas. BATTERY SITE, COMPRESSOR SITE,
    FLARE STACK, METER STATION SITE, and VALVE SITE.
-   **OIL-GAS-PLANT;** a numeric variable indicating the proportion of
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
-   **RIS-CAMP-INDUSTRIAL;** a numeric variable indicating the
    proportion of areas disturbed for the purposed of housing camp
    workers within the buffer area.
-   **RIS-CLEARING-UNKNOWN:** a numeric variable indicating proportion
    of the buffer area. Identifies all areas where vegetation has been
    removed for the purposes of preparing the land for drainage, soil
    removal, overburden removal, mining, etc. but where soil has been
    left mostly intact and relatively undisturbed. May include any or
    all of: tree removal, shrub removal, and/or grubbing (stump
    removal). Identifies areas cleared for by other industries and not
    for the purposes of forest harvesting or for oil sands development.
-   **RIS-DRAINAGE:** a numeric variable indicating proportion of the
    buffer area. Identifies surface disturbance for the purpose of
    managing surface water features.
-   **RIS-FACILITY-OPERATIONS:** a numeric variable indicating
    proportion of the buffer area. Designated for areas which are not
    part of the plant site, e.g., may include laydown areas not
    integrated with the main plant site(s), tailings lines, water lines,
    compressor station, buildings away from the main plant site, flare
    stack, communications tower.
-   **RIS-FACILITY-UNKNOWN:** a numeric variable indicating proportion
    of the buffer area. Identifies areas where the reclamation liability
    associated for the disturbance is currently held by another industry
    operator.
-   **RIS-MINES-OILSANDS:** a numeric variable indicating proportion of
    the buffer area. Identifies areas where overburden removal has
    commenced for the purposes of preparing an area for open pit mining
    and all mine pit features.
-   **RIS-OILSANDS-RMS:** a numeric variable indicating proportion of
    the buffer area. Identifies reclamation material stockpiles (RMS).
    Each RMS may have several material types and corresponding volumes.
-   **RIS-OVERBURDEN-DUMP:** a numeric variable indicating proportion of
    the buffer area. Includes all areas where overburden and interburden
    is placed out-of-pit or in-pit for disposal.
-   **RIS-RECLAIMED-PERMANENT:** a numeric variable indicating
    proportion of the buffer area. Identifies polygons which meet the
    definition of permanent reclamation - land is considered permanently
    reclaimed when landform construction and contouring, clean material
    placement (as required), reclamation material placement and
    revegetation has taken place.
-   **RIS-RECLAIMED-TEMP:** a numeric variable indicating proportion of
    the buffer area. Identifies polygons which meet the definition of
    temporary reclamation -- areas being managed where vegetation has
    been seeded, planted, or ingressed, where there is an expectation
    that future disturbance may occur at that location. This does not
    include cleared areas (planned for future disturbance) that have
    naturally revegetated through ingress.
-   **RIS-ROAD:** a numeric variable indicating proportion of the buffer
    area. Identifies roads that are not specifically part of other
    disturbed features in oil sand mines area only.
-   **RIS-SOIL-REPLACED:** a numeric variable indicating proportion of
    the buffer area. Identifies areas which have had subsoil or topsoil
    placed and which have not been revegetated.
-   **RIS-SOIL-SALVAGED:** a numeric variable indicating proportion of
    the buffer area. Identifies areas where soil salvage is occurring
    but where overburden removal has not commenced.
-   **RIS-TAILING-POND:** a numeric variable indicating proportion of
    the buffer area. Identifies all areas associated with tailings
    including toe berms, dykes, beaches, ponds and drying areas.
-   **RIS-TRANSMISSION-LINE:** a numeric variable indicating proportion
    of the buffer area. Include the right of way area designated for the
    power line.
-   **RIS-UTILITIES:** a numeric variable indicating proportion of the
    buffer area. Identifies areas specifically disturbed for the
    purposes of utilities (power generation).
-   **RIS-WINDROW:** a numeric variable indicating proportion of the
    buffer area. Includes areas where a line of reclamation material
    (soil or vegetation) is heaped up by a machine.
-   **RLWY-SGL-TRACK;** a numeric variable indicating the proportion of
    single track railways within the buffer area. Single track railways
    are defined as, hard, steel rail lines designed for train use.
    Specifically, a road or track for trains, consisting of parallel
    steel rails, supported on wooden crossbeams. The single track
    consists of one parallel sets of tracks.
-   **ROAD-GRAVEL-1L;** a numeric variable indicating the proportion of
    1L gravel roads within the buffer area. 1L gravel roads are defined
    as, a roadway surfaced with gravel constituting a main access route.
    The road surface is about 6 meters in width, and the road clearing
    is about 20 meters or greater in width. The surface, ditches,
    bridges and intersections are in good condition.
-   **ROAD-GRAVEL-2L;** a numeric variable indicating the proportion of
    2L gravel roads within the buffer area. 2L gravel roads are defined
    as, a roadway surfaced with gravel constituting as a main access
    route. The road surface is 7 meters or greater in width, and the
    road clearing is 30 meters or greater in width. The surface,
    ditches, bridges and intersections are in good condition.
-   **ROAD-PAVED-DIV;** a numeric variable indicating the proportion of
    PAVED-DIV roads within the buffer area. PAVED-DIV roads are defined
    as, a major roadway, which is paved with asphalt or concrete, and
    consists of two (2) roadbeds separated by a median. Each road bed
    usually consists of two (2) or more lanes.
-   **ROAD-PAVED-UNDIV-1L;** a numeric variable indicating the
    proportion of UNDIV 1L paved roads within the buffer area. UNDIV 1L
    paved roads are defined as, non-vegetated, impermeable surfaces used
    for motorized vehicle or aircraft transportation or access.
    Specifically, a roadway, paved with asphalt or concrete, consisting
    of one (1) lane, and usually found servicing rural acreages that are
    close to large urban centers.
-   **ROAD-PAVED-UNDIV-2L;** a numeric variable indicating the
    proportion of 2L paved roads within the buffer area. 2L paved roads
    are defined as, non-vegetated, impermeable surfaces used for
    motorized vehicle or aircraft transportation or access.
    Specifically, a major roadway, which is paved with asphalt or
    concrete, and consists of two (2) roadbeds separated by a median.
    Each road bed usually consists of two (2) or more lanes.
-   **ROAD-UNCLASSIFIED;** a numeric variable indicating the proportion
    of unclassified roads within the buffer area. Unclassified roads are
    defined as, non-vegetated, impermeable surfaces used for motorized
    vehicle or aircraft transportation or access. Specifically, a
    temporary coding for an unknown class of road, which will be updated
    after a field check or verification.
-   **ROAD-UNIMPROVED;** a numeric variable indicating the proportion of
    unimproved roads within the buffer area. Unimproved roads are
    defined as, a roadway surfaced with dirt, which is constituted as a
    minor access route. The road surface is up to 7 meters in width, and
    the road clearing is up to 20 meters in width. The surface and
    ditches are poorly maintained, and the bridges are narrow.
-   **ROAD-WINTER;** a numeric variable indicating the proportion of
    winter roads within the buffer area. Winter roads are defined as,
    non-vegetated, impermeable surfaces used for motorized vehicle or
    aircraft transportation or access. Specifically, a clearing that is
    vehicular accessible in winter only.
-   **ROUGH_PASTURE;** a numeric variable indicating the proportion of
    rough pasture within the buffer area. Rough pasture is defined as,
    lands where the forest and/or shrubs have been removed so that
    native or introduced grasses can flourish for the grazing of
    livestock. Specifically, this pastureland has not been irrigated or
    fertilized and the soil has not been disturbed to improve
    productivity.
-   **RUNWAY;** numeric variable indicating the proportion of
    unclassified runways within the buffer area. Runways are defined as,
    human footprint related to vegetated facilities and recreation,
    specifically a vegetated runway.
-   **RURAL-RESIDENCE;** a numeric variable indicating the proportion of
    rural residence within the buffer area. Rural residence is defined
    as, country-residential developments with density of 10 - 100
    buildings per quarter section.
-   **SUMP;** a numeric variable indicating the proportion of sumps
    within the buffer area. Sumps are defined as, An artificial holding
    or treatment pond for industrial wastewater. Drilling waste storage
    system -- holding of drilling waste on well sites or remotely.
    Either earthen excavation (in clayey soils) or sumps lined with a
    synthetic liner.
-   **SURROUNDING-VEG;** a numeric variable indicating the proportion of
    surrounding vegetation within the buffer area. Surrounding
    vegetation is defined as, human footprint related to vegetated
    facilities and recreation. Specifically, disturbed vegetation
    surrounding airport runways, highway ramps and other industrial
    features.
-   **TAILING-POND;** a numeric variable indicating the proportion of
    tailing pond within the buffer area. Tailing pond is defined as,
    body of water on/in close proximity to an oil sands mine comprising
    acids, benzene, hydrocarbons, residual bitumen, fine silts, and
    water.
-   **TAME_PASTURE;** a numeric variable indicating the proportion of
    tame pasture within the buffer area. Tame pasture is defined as,
    lands where the soil has been disturbed and planted to perennial
    grass species used primarily for grazing livestock. Specifically,
    tame pasture represents areas of grasses, legumes or grass-legume
    mixtures planted for livestock grazing or hay collection.
-   **TRAIL;** a numeric variable indicating the proportion of trails
    within the buffer. Trails are defined as, a polygon feature class
    derived from a 2-meter buffer (4 meter total width) of a
    pre-low-impact-seismic centerline.
-   **TRANSMISSION-LINE;** a numeric variable indicating the proportion
    of transmission lines within the buffer area. Transmission lines are
    defined as, cleared corridors designated for the location of power
    transmission line infrastructure.
-   **TRUCK-TRAIL;** a numeric variable indicating the proportion of
    truck trails within the buffer area. Truck trails are defined as, a
    roadway surfaced with dirt or low vegetation constituting a minor
    access route.
-   **URBAN-INDUSTRIAL;** a numeric variable indicating the proportion
    of urban-industrial area within the buffer area. Urban-industrial
    area is defined as, human footprint features related to various
    industrial activities. Specifically, an industrial facility within
    the boundary of an urban residence.
-   **URBAN-RESIDENCE;** a numeric variable indicating the proportion of
    urban residence within the buffer area. Urban residence is defined
    as, residential areas in cities, towns, villages, hamlets and ribbon
    developments. Areas that are dominated by dwellings.
-   **VEGETATED-EDGE-RAILWAYS;** a numeric variable indicating the
    proportion of vegetated edge railways within the buffer area.
    Vegetated edge railways are defined as, disturbed vegetation
    alongside road edges and railway edges including ditches.
-   **VEGETATED-EDGE-ROADS;** a numeric variable indicating the
    proportion of vegetated edge roads within the buffer area. Vegetated
    edge roads are defined as, disturbed vegetation alongside road edges
    and railway edges including ditches.
-   **WELL-ABAND;** a numeric variable indicating the proportion of
    abandoned wells within the buffer. Abandoned wells are defined as,
    ground cleared for an oil/gas well pad where the well is currently
    abandoned.
-   **WELL-BITUMEN;** a numeric variable indicating the proportion of
    bitumen wells within the buffer area. Bitumen wells are defined as,
    ground cleared for an oil/gas well pad where at least one well is
    currently active.
-   **WELL-CASED;** a numeric variable indicating the proportion of
    bitumen wells within the buffer area. Bitumen wells are defined as,
    ground cleared for an oil/gas well pad where at least one well is
    currently active.
-   **WELL-GAS;** a numeric variable indicating the proportion of gas
    wells within the buffer area. Gas wells are defined as, ground
    cleared for an gas well pad where at least one well is currently
    active.
-   **WELL-OIL;** a numeric variable indicating the proportion of oil
    wells within the buffer. Oil wells are defined as, ground cleared
    for an oil well pad where at least one well is currently active.
-   **WELL-OTHER;** a numeric variable indicating the proportion of
    other wells within the buffer area. Other wells are defined as,
    ground cleared for an oil/gas well pad where at least one well is
    currently active.
-   **WELL-UNKNOWN;** a numeric variable indicating the proportion of
    unknown wells within the buffer area. Unknown wells are defined as,
    ground cleared for an oil/gas well pad where at least one well is
    currently active. Specifically, a ell site - ground cleared, well
    status unknown or license location.
-   **WELL_CLEARED_NOT_CONFIRMED;** a numeric variable indicating the
    proportion of unconfirmed wellpad clearings within the buffer area.
    Unconfirmed wellpad clearings are defined as, human footprint
    features related to various industrial activities. Specifically,
    Roughly square in shape clearing, roughly 90-120 meters wide
    (approximately 1 ha). Not confirmed as a well pad by available
    reference sources.
-   **WELL_CLEARED_NOT_DRILLED;** a numeric variable indicating the
    proportion of not drilled wells within the buffer area. Not drilled
    wells are defined as, ground cleared for an oil/gas well pad where
    at least one well is currently active. Specifically, a well site -
    confirmation of the boundary outline is provided by reference
    sources.

### DATA-SPECIFIC INFORMATION FOR: [OSM_independent_detections_2021_2022_2023.csv]

-   **Number of variables:** 8
-   **Number of cases/rows:** 34,540
-   **NOTES:** each row corresponds to a new independent detection.

**Variable List:**

-   **array;** a factor with 10 levels describing the landscape unit
    (eg., LU01)
-   **camera;** a factor with 430 levels describing the camera site
-   **site;** a factor with 430 levels where the first element
    abbreviation describes the landscape unit and the second element
    describes the camera site.
-   **species;** species present in the independent event
-   **event_start;** independent detection start date/time, format:
    YYYY-MM-DD HH:MM:SS
-   **event_end;** independent detection end date/time, format:
    YYYY-MM-DD HH:MM:SS
-   **year:** year in which the independent event was captured
-   **month;** month in which the independent event was captured (1 to
    12).

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
    format: YYYY-MM-DD

### DATA-SPECIFIC INFORMATION FOR: [OSM_simple_config_landscapemetrics.csv]

-   **Number of variables:** 15
-   **Number of cases/rows:** 9461
-   **NOTE:** An intermediate file wherein all variables used in final
    analysis are decribed under
    "processed/OSM_all_covariates_HFI_SBFI_final.csv"

### DATA-SPECIFIC INFORMATION FOR: [OSM_timelapse_2021.csv], [OSM_timelapse_2022.csv], and [OSM_timelapse_2023.csv]

-   **Number of variables:** 42
-   **Number of cases/rows:** 80,649 [OSM_timelapse_2021.csv], 316,635
    [OSM_timelapse_2022.csv], 285,978 [OSM_timelapse_2023.csv].
-   **NOTE:** all three Timelapse files were processed using the same
    CodeTemplate (see <https://timelapse.ucalgary.ca/>) and contain the
    exact same columns. Each file represents a new year of data.

**Variable List:**

-   **file**, character with the name of the original camera image
-   **relativepath**, character with the relative path of the image
    compared to the .ddb file
-   **datetime**, datetime, the date and time the image was taken. A
    leading space has been added to prevent parsing issues in MS Excel.
-   **array**, factor describing the landscape unit of a camera (i.e.
    LU09, LU16, LU14, or LU22).
-   **camera**, factor describing the identity of the camera site within
    an array
-   **site**, factor where the first element abbreviation describes the
    landscape unit and the second element describes the camera site.
-   **classifier**, character, the person who tagged the image data
-   **snow**, factor, the percent snow cover on the ground in the image
-   **species**, factor, the identity of the species present in the
    image
-   **total**, numeric, the total number of animals in the image
-   **male**, numeric, the total number of male animals in the image.
    Only for animals larger than coyotes.
-   **female**, numeric, the total number of female animals in the
    image. Only for animals larger than coyotes.
-   **unknownsex**, numeric, the total number of animals with
    unidentifiable sex in the image. Only for animals larger than
    coyotes.
-   **adult**, numeric, the total number of adult animals in the image.
    Only for animals larger than coyotes.
-   **yly**, numeric, the total number of yearling animals in the image.
    Only for animals larger than coyotes.
-   **yoy**, numeric, the total number of young of year animals in the
    image. Only for animals larger than coyotes.
-   **unknownage**, numeric, the total number of animals with
    unidentifiable age in the image. Only for animals larger than
    coyotes.
-   **group_count**, numeric, the total number of animals in the event
    image sequence (see event column)
-   **g_male**, numeric, the total number of male animals in the event
    image sequence (see event column). Only for animals larger than
    coyotes.
-   **g_female**, numeric, the total number of female animals in the
    event image sequence (see event column). Only for animals larger
    than coyotes.
-   **g_unknownsex**, numeric, the total number of animals with
    unidentifiable sex in the event image sequence (see event column).
    Only for animals larger than coyotes.
-   **g_adult**, numeric, the total number of adult animals in the event
    image sequence (see event column). Only for animals larger than
    coyotes.
-   **g_yly**, numeric, the total number of yearling animals in the
    event image sequence (see event column). Only for animals larger
    than coyotes.
-   **g_yoy**, numeric, the total number of young of year animals in the
    event image sequence (see event column). Only for animals larger
    than coyotes.
-   **gunknownage**, numeric, the total number of animals with
    unidentifiable age in the event image sequence (see event column).
    Only for animals larger than coyotes.
-   **event**, factor, indicates the first and last image in an event.
    An "event" is a continuous sequence of images where fewer than 60
    seconds pass between two successive images. Singleton events are not
    tagged.
-   **empty**, logical, whether an animal is present in the image
-   **coatcolor**, factor, the coat color of one of the animals in the
    image. Only for bears, wolves, and foxes.
-   **leftantler**, factor, the number of left antler tines for
    ungulates. Only for specific months (species specific)
-   **rightantler**, factor, the number of right antler tines for
    ungulates. Only for specific months (species specific)
-   **lcount**, factor, whether the left tine count is a total or
    minimum estimate.
-   **rcount**, factor, whether the right tine count is a total or
    minimum estimate.
-   **comments**, character, miscellaneous comments about the image
-   **otherspecify**, character, details when 'other' is entered for
    species or camera malfunction
-   **cameramalfunction**, factor, details about camera errors such as
    trigger malfunction or repositioning
-   **noteworthy**, logical, whether the photo is noteworthy and should
    be saved for reporting
-   **fullpath**, character, the filepath to the original image on the
    Netdrive
-   **datasource**, character, the filepath to the original .ddb on the
    Netdrive containing the image data
-   **month**, numeric, month the image was taken
-   **day**, numeric, day the image was taken
-   **year**, numeric, year the image was taken
