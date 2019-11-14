# Ohio Election Shapefile
This shapefile was compiled and processed by members of the Voting Rights Data Institute (VRDI) and the Metric Geometry and Gerrymandering Group (MGGG). VRDI was a 2018 summer intensive sponsored by MGGG at Tufts and MIT, with major support from a Bose Research Grant at MIT and from the Jonathon M. Tisch College of Civic Life at Tufts.

## Sources
Raw data for Ohio's precinct boundaries was sourced from election and other county officials and processed by members of MGGG and students at VRDI. For more information on the sourcing of this data, please refer to the Metric Geometry and Gerrymandering Group's [Ohio Precincts Github repository](https://github.com/mggg/ohio-precincts). Election data come the [Ohio Secretary of State](https://www.sos.state.oh.us/elections/election-results-and-data/2016-official-elections-results/) and the [MIT Election Data Science Lab](https://electionlab.mit.edu). Demographic data were downloaded at the census block level from [IPUMS NHGIS](https://www.nhgis.org).

## Preprocessing
Demographic data were aggregated from the block level using MGGG’s proration software [maup](https://github.com/mggg/maup). Congressional, house, and senate district IDs were assigned to precincts also using this package.

## Metadata
* `CNTYFIPS`: County FIPS code
* `COUNTY`: County name
* `CODE`: County-level precinct code
* `PRECODE`: County FIPS and precinct code (precinct unique identifier)
* `PRECINCT`: Precinct name
* `PRENAME`: Precinct name from tabular results
* `TOTREG16`: Total registered voters on November 8, 2016
* `TOTVOTE16`: Total votes cast on November 8, 2016
* `TURNOUT16`: Turnout proportion on November 8, 2016
* `PRES16R`: Number of votes for 2016 Republican presidential candidate
* `PRES16D`: Number of votes for 2016 Democratic presidential candidate
* `PRES16L`: Number of votes for 2016 Libertarian presidential candidate
* `PRES16G`: Number of votes for 2016 Green Party presidential candidate
* `SEN16R`: Number of votes for 2016 Republican senate candidate
* `SEN16D`: Number of votes for 2016 Democratic senate candidate
* `USH16R`: Number of votes for 2016 Republican US congressional candidates
* `USH16D`: Number of votes for 2016 Democratic US congressional candidates
* `SSEN16R`:  Number of votes for 2016 Republican state senate candidates
* `SSEN16D`:  Number of votes for 2016 Democratic state senate candidates
* `STH16D`:  Number of votes for 2016 Republican state house candidates
* `STH16R`:  Number of votes for 2016 Democratic state house candidates
* `TOTPOP`: Total population 
* `NH_WHITE`: White, non-hispanic, population
* `NH_BLACK`: Black, non-hispanic, population
* `NH_AMIN`: American Indian and Alaska Native, non-hispanic, population
* `NH_ASIAN`: Asian, non-hispanic, population
* `NH_NHPI`: Native Hawaiian and Pacific Islander, non-hispanic, population
* `NH_OTHER`: Other race, non-hispanic, population
* `NH_2MORE`: Two or more races, non-hispanic, population
* `HISP`: Hispanic population
* `H_WHITE`: White, hispanic, population
* `H_BLACK`: Black, hispanic, population
* `H_AMIN`: American Indian and Alaska Native, hispanic, population
* `H_ASIAN`: Asian, hispanic, population
* `H_NHPI`: Native Hawaiian and Pacific Islander, hispanic, population
* `H_OTHER`: Other race, hispanic, population
* `H_2MORE`: Two or more races, hispanic, population
* `VAP`: Total voting age population
* `HVAP`: Hispanic voting age population
* `WVAP`: White, non-hispanic, voting age population
* `BVAP`: Black, non-hispanic, voting age population
* `AMINVAP`: American Indian and Alaska Native, non-hispanic, voting age population
* `ASIANVAP`: Asian, non-hispanic, voting age population
* `NHPIVAP`: Native Hawaiian and Pacific Islander, non-hispanic, voting age population
* `OTHERVAP`: Other race, non-hispanic, voting age population
* `2MOREVAP`: Two or more races, non-hispanic, voting age population
* `CD`: US congressional district ID
* `SEND`: State Senate district ID
* `HDIST`: State House district ID

## Projection
This shapefile uses a NAD83(Harn)/UTM zone 17 North projection (EPSG:3747).
