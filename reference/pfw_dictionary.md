# Look Up Definitions from the Project FeederWatch Data Dictionary

This function helps users explore the FeederWatch dataset by viewing the
full data dictionary or searching for definitions for specific
variables.

## Usage

``` r
pfw_dictionary(variable = NULL)
```

## Arguments

- variable:

  (Optional) A variable name (e.g., "LOC_ID") to look up. If NULL,
  prints the full dictionary.

## Value

A printed description (for a variable) or the full dictionary.

## Examples

``` r
# View the whole data dictionary
pfw_dictionary()
#> Variable:   LOC_ID
#> Definition: Unique identifier for each survey site
#> Description:Each observation location should have only one LOC_ID. A single observer may maintain more than one LOC_ID. This is the same field as LOC_ID in the site description dataset and can be used to link the observation data to the site description data in conjunction with PROJ_PERIOD_ID.
#> 
#> Variable:   LATITUDE
#> Definition: Latitude in decimal degrees for each survey site
#> Description:Accuracy varies. See ENTRY_TECHNIQUE below. 
#> 
#> Variable:   LONGITUDE
#> Definition: Longitude in decimal degrees for each survey site
#> Description:Accuracy varies. See ENTRY_TECHNIQUE below. 
#> 
#> Variable:   SUBNATIONAL1_CODE
#> Definition: Country abbreviation and State or Province abbreviation of each survey site
#> Description:Format XX-XX where the left two letters indicate the country and the right two letters indicate the state or province code. E.g., CA-ON = Canada - Ontario
#> 
#> Variable:   ENTRY_TECHNIQUE
#> Definition: Variable indicating method of site localization
#> Description:Codes represent dozens of methods for site creation with varying degrees of specificity. These methods continue to evolve as online mapping technologies change. The most accurate locations have higher "zoom level" values (e.g., Google Map Zoom level 9). Note that postal code locations were geolocated at the centroid of the postal code within which the site is located (i.e., these sites lack accuracy and are not useful if you are trying to link to site to satellite-derived land cover data, for instance).
#> 
#> Variable:   SUB_ID
#> Definition: Unique identifier for each checklist
#> Description:
#> 
#> Variable:   OBS_ID
#> Definition: Unique identifier for each observation of a species
#> Description:One SUB_ID will have as many OBS_ID values as there were species reported on a given checklist. 
#> 
#> Variable:   MONTH
#> Definition: Month of 1st day of two-day observation period
#> Description:
#> 
#> Variable:   DAY
#> Definition: Day of 1st day of two-day observation period
#> Description:
#> 
#> Variable:   YEAR
#> Definition: Year of 1st day of two-day observation period
#> Description:
#> 
#> Variable:   PROJ_PERIOD_ID
#> Definition: Calendar year of end of FeederWatch season
#> Description:In the format 'PFW_2019' where PFW = Project FeederWatch. The year indicates the FeederWatch season which is defined as the year the season ended. E.g., the November 2018 through April 2019 season is labeled 'PFW_2019'. This is the same field as PROJ_PERIOD_ID in the site description dataset and can be used to link the observation data to the site description data in conjunction with LOC_ID.
#> 
#> Variable:   SPECIES_CODE
#> Definition: Bird species observed, stored as 6-letter species codes
#> Description:Species codes are based on the eBird taxonomy. See "Species Codes" tab below for code translations. 
#> 
#> Variable:   alt_full_spp_code
#> Definition: Alternate code for bird species observed, lumping subspecies/recognizable forms
#> Description:This column enables someone to "roll up" information on subspecies and recognizable forms into the species code of the full species instead of the code for the recognizable form. The species code values for the subspecies/forms are still the primary information stored in the column SPECIES_CODE, but the alternate code for the full species is available in the column immediately to its right.
#> 
#> Variable:   HOW_MANY
#> Definition: Maximum number of individuals seen at one time during observation period
#> Description:
#> 
#> Variable:   VALID
#> Definition: Validity of each observation based on flagging system
#> Description:1 = observation did not trigger the automated review system or was reviewed and approved. 0 = observation triggered the automated review system and has either not been reviewed or was reviewed and left as 'invalid'. Use 0 records with extreme caution. Details of the review process: Bonter, D.N. and C.B. Cooper. 2012. Data validation in citizen science: A case study from Project FeederWatch. Frontiers in Ecology and the Environment 10:305-307.
#> 
#> Variable:   REVIEWED
#> Definition: Review state of each observation based on flagging system
#> Description:1 = observation was reviewed by FeederWatch staff. 0 = observation either did not trigger the automated review system or has not yet been reviewed. Details of the review process: Bonter, D.N. and C.B. Cooper. 2012. Data validation in citizen science: A case study from Project FeederWatch. Frontiers in Ecology and the Environment 10:305-307.
#> 
#> Variable:   PLUS_CODE
#> Definition: Variable indicating if the total number of a species seen was larger than the value reported
#> Description:Data field used on historic paper data forms (no longer being populated). Due to space limitations of the paper forms, some large flock sizes could not be recorded accurately. In such a case, the "PLUS_CODE" field is coded as '1', indicating that the number of birds seen was larger than that reported in the "HOW_MANY" field. Observations where PLUS_CODE = 1 and HOW_MANY = 9, 90, 99, or 999 should be used with caution. 
#> 
#> Variable:   DAY1_AM
#> Definition: Variable indicating if observer watched during morning of count Day 1
#> Description:0 = observer did not watch their feeders during the morning of Day 1; 1 = observer did watch their feeders during this time interval. We suggest adding the values in the DAY1_AM, DAY1_PM, DAY2_AM and DAY2_PM fields into an aggregated measure of effort indicating the number of half days of observation effort (range = 1-4). 
#> 
#> Variable:   DAY1_PM
#> Definition: Variable indicating if observer watched during afternoon of count Day 1
#> Description:See DAY1_AM
#> 
#> Variable:   DAY2_AM
#> Definition: Variable indicating if observer watched during morning of count Day 2
#> Description:See DAY1_AM
#> 
#> Variable:   DAY2_PM
#> Definition: Variable indicating if observer watched during afternoon of count Day 2
#> Description:See DAY1_AM
#> 
#> Variable:   EFFORT_HRS_ATLEAST
#> Definition: Participant estimate of survey time  for each checklist
#> Description:A second measure of observation effort. Categorical: 0.001 = less than 1 hour of observation during the 2-day count period;   1.001 = 1 to 4 hours of observation; 4.001 = 4 to 8 hours of observation; 8.001 = greater than 8 hours of observation. 
#> 
#> Variable:   SNOW_DEP_ATLEAST
#> Definition: Participant estimate of minimum snow depth during a checklist
#> Description:An estimate of snow depth. Categorical: . = null; 0 = none; 0.001 = less than 5 cm; 5.000 = 5 to 15 cm; 15.001 = greater than 15 cm
#> 
#> Variable:   DATA_ENTRY_METHOD
#> Definition: Data entry method for each checklist (e.g., web, mobile app or paper form)
#> Description:As of 2020, the three modes of data entry for the dataset include paper data forms (field value indicates 'paper'), the FeederWatch website (field value indicates various versions of 'Web' entry), or the mobile phone app (field value indicates various versions of 'Mobile' entry). 
#> 
#> Variable:   Yard_type
#> Definition: Variables indicating features of yard (*five fields)
#> Description:0 = absent, 1 = present for each category of yard type: Pavement (no vegetation), garden or courtyard, landscaped yard, natural vegetation, natural or landscaped desert.
#> 
#> Variable:   Habitat_type
#> Definition: Variables indicating features of surrounding habitat (*fourteen fields)
#> Description:0 = absent, 1 = present for the following habitat types located within 0.5 miles of the count site: deciduous woods, evergreen woods, mixed deciduous-evergreen woods, orchard, park, fresh water, salt water, residential area, industrial or commercial, agricultural fields, desert or scrub, secondary growth woods, swamp (wooded), marsh).
#> 
#> Variable:   Trees/shrubs
#> Definition: Variables indicating types of surrounding vegetation (*six fields)
#> Description:Minimum number of trees or shrubs of various types within the count area. EVGR = evergreen; DCID = deciduous, FRU = fruit, CACTI = cacti. Note that this field has been inconsistently recorded over time. Current (2020) categories: 0, 1-3, 4-10, > 10.
#> 
#> Variable:   Brush/water
#> Definition: Variables indicating presence of brush piles or water sources (*three fields)
#> Description:Categorical. Minimum number of brush piles, water sources, and bird baths located within the count area. Note that categories changed slightly over the years. Generally, categories represent: 0, 1-3, 4-10, > 10.
#> 
#> Variable:   NEARBY_FEEDERS
#> Definition: Variable indicating if other feeders are regularly operated within 90m of survey site
#> Description:Present or absence of feeders (others than those maintained by the participant) within 90 m of the count site. 0 = feeders absent, 1 = feeders present. 
#> 
#> Variable:   Other_animals
#> Definition: Variables indicating if squirrels, cats, dogs or humans are at the survey site (*four fields)
#> Description:0 = no, 1 = yes. Do squirrels take food from feeders at least 3 times per week? Are cats, dogs, or humans active within 30 m of the feeders for at least 30 minutes 3 days per week? 
#> 
#> Variable:   HOUSING_DENSITY
#> Definition: Participant estimated housing density of neighborhood
#> Description:Participant-defined description of the housing density of the neighborhood. 1 = "rural", 2 = "rural/suburban", 3 = "suburban", 4 = "urban"
#> 
#> Variable:   Feeding_schedule
#> Definition: Variables indicating which months of the year participants provide food (*thirteen fields)
#> Description:0 = no, 1 = yes. Response to the following question for each month, "I provided food in my count site at least once per week." Note that the field indicating whether or not the participant provides food year-round (FED_YR_ROUND) has not be consistently applied throughout the history of the project. 
#> 
#> Variable:   Feeder_numbers_by_type
#> Definition: Variables indicating the number and types of feeders provided (*eight fields)
#> Description:Participants report the number of feeders maintained within their count site. Suet or fat feeders, ground feeding sites, hanging feeders, platform feeders, sugar water feeders (HUMMING), water dispensers (field retired in 2005), thistle feeders (field retired in 2005), fruit feeders. 
#> 
#> Variable:   POPULATION_ATLEAST
#> Definition: Participant estimated population of city or town
#> Description:1 = less than 5,000; 5001 = 5,001 - 25,000; 25001 = 25,001 - 100,000; 100001 = > 100,000.
#> 
#> Variable:   COUNT_AREA_SIZE_SQ_M_ATLEAST
#> Definition: Participant estimated area of survey site
#> Description:0.01 = < 1 square meter; 1.01 = 1 to 100 square meters; 100.01 = 100 - 375 square meters; 375.01 = > 375 square meters
#> 
#> Variable:   CREATION_DT
#> Definition: Date of site creation
#> Description:All sites created prior to 2001 are listed as created in 2001.
#> 
#> Variable:   LAST_EDITED_DT
#> Definition: Date of last site location edit
#> Description:Lists the most recent date site-specific data was edited.
#> 
#> Variable:   supp_food
#> Definition: Participant indicates whether supplementary food was provided (1) or not provided (0) at the site
#> Description:Variable added during the 2021-2022 FeederWatch season, this variable allows people to indicate if they watched birds within a fixed area but did not provide supplemental food (i.e., watching an area that they landscaped for birds but with no direct bird feeding). 1 = supplemental food provided, 0 = supplemental food NOT provided, null before the 2021-22 season could be interpreted as food provided because FeederWatch was explicitly focused on bird feeding stations. 
#> 

# View the data dictionary entry for location ID ("LOC_ID")
pfw_dictionary("LOC_ID")
#> Variable:   LOC_ID
#> Definition: Unique identifier for each survey site
#> Description:Each observation location should have only one LOC_ID. A single observer may maintain more than one LOC_ID. This is the same field as LOC_ID in the site description dataset and can be used to link the observation data to the site description data in conjunction with PROJ_PERIOD_ID.
```
