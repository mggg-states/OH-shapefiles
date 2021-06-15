# Ohio Election Shapefile
The shapefile is a lightly edited VTD. Edits are based on more recent shapefiles from counties. A few precincts were merged to match election results.
This shapefile was compiled and processed by the Metric Geometry and Gerrymandering Group (MGGG). 

## Sources
Raw data for Ohio's precinct boundaries was sourced from election and other county officials and processed by members of MGGG and students at VRDI. For more information on the sourcing of this data, please refer to the Metric Geometry and Gerrymandering Group's [Ohio Precincts Github repository](https://github.com/mggg/ohio-precincts). Election data come the [Ohio Secretary of State](https://www.sos.state.oh.us/elections/election-results-and-data/2016-official-elections-results/) and the [MIT Election Data Science Lab](https://electionlab.mit.edu). Demographic data were downloaded at the census block level from [IPUMS NHGIS](https://www.nhgis.org).

## Preprocessing
Demographic data were aggregated from the block level using MGGG’s proration software [maup](https://github.com/mggg/maup). Congressional, house, and senate district IDs were assigned to precincts also using this package.

## Notes
Election abbreviations are all according to our codes except supreme court justices. Those are SCJ. There's SCJ20D1/R1, SCJ20D2/R2, and SCJ20D/R. The ones without numbers are summed by party. 1 is the O'Donnell/Kennedy race, 2 is Brunner/French. You can read more about this on [Ballotpedia](https://ballotpedia.org/Ohio_Supreme_Court), but Ohio Supreme Court elections are technicallly nonpartisan and they come out of a partisan primary so it's basically a partisan in practice even if it's not official.

For population breakdowns, anything ending in '19' (example NH_WHITE19) is taken from American Community Survey 5-year estimates (2014-2019). Anything ending in '10' (example NH_WHITE10) is taken from the decennial census data.

## Metadata
* `STATEFP20`: State FIPS code
* `COUNTYFP20`: County FIPS code
* `VTDST20`: VTD code
* `COUNTY`: County name
* `CODE`: County-level precinct code
* `PRECODE`: County FIPS and precinct code (precinct unique identifier)
* `PRECINCT`: Precinct name
* `PRENAME`: Precinct name from tabular results
* `TOTREG16`: Total registered voters on November 8, 2016
* `TOTVOTE16`: Total votes cast on November 8, 2016
* `TURNOUT16`: Turnout proportion on November 8, 2016
* `PRES20D`: Number of votes for 2020 Democratic presidential candidate
* `PRES20R`: Number of votes for 2020 Republican presidential candidate
* `USH20D`: Number of votes for 2020 Democractic US congressional candidates
* `USH20R`: Number of votes for 2020 Republican US congressional candidates
* `SCJ20D`: Number of votes for 2020 Democractic Supreme Court Justice 
* `SCJ20R`: Number of votes for 2020 Republican Supreme Court Justice
* `SCJ20D1`: Number of votes for 2020 Democractic Supreme Court Justice (O'Donnell/Kennedy race)
* `SCJ20R1`: Number of votes for 2020 Republican Supreme Court Justice (O'Donnell/Kennedy race)
* `SCJ20D2`: Number of votes for 2020 Democratic Supreme Court Justice (Brunner/French) 
* `SCJ20R2`: Number of votes for 2020 Republican Supreme Court Justice (Brunner/French) 
* `PRES16R`: Number of votes for 2016 Republican presidential candidate
* `PRES16D`: Number of votes for 2016 Democratic presidential candidate
* `PRES16L`: Number of votes for 2016 Libertarian presidential candidate
* `PRES16G`: Number of votes for 2016 Green Party presidential candidate
* `SEN16R`: Number of votes for 2016 Republican senate candidate
* `SEN16D`: Number of votes for 2016 Democratic senate candidate
* `USH16D`: Number of votes for 2016 Republican US congressional candidates
* `USH16R`: Number of votes for 2016 Democratic US congressional candidates
* `SSEN16R`:  Number of votes for 2016 Republican state senate candidates
* `SSEN16D`:  Number of votes for 2016 Democratic state senate candidates
* `STH16D`:  Number of votes for 2016 Republican state house candidates
* `STH16R`:  Number of votes for 2016 Democratic state house candidates
* `CD`: US congressional district ID
* `SEND`: State Senate district ID
* `HDIST`: State House district ID
* `TOTPOP`: Total population 
* `NH_WHITE19`: White, non-hispanic, population
* `NH_BLACK19`: Black, non-hispanic, population
* `NH_AMIN19`: American Indian and Alaska Native, non-hispanic, population
* `NH_ASIAN19`: Asian, non-hispanic, population
* `NH_NHPI19`: Native Hawaiian and Pacific Islander, non-hispanic, population
* `NH_OTHER19`: Other race, non-hispanic, population
* `NH_2MORE19`: Two or more races, non-hispanic, population
* `HISP19`: Hispanic population
* `H_WHITE19`: White, hispanic, population
* `H_BLACK19`: Black, hispanic, population
* `H_AMIN19`: American Indian and Alaska Native, hispanic, population
* `H_ASIAN19`: Asian, hispanic, population
* `H_NHPI19`: Native Hawaiian and Pacific Islander, hispanic, population
* `H_OTHER19`: Other race, hispanic, population
* `H_2MORE19`: Two or more races, hispanic, population
* `VAP19`: Total voting age population
* `VAP10`: Total Voting Age Population
* `NH_WHITE10`: White, non-hispanic, population
* `NH_BLACK10`: Black, non-hispanic, population
* `NH_AMIN10`: American Indian and Alaska Native, non-hispanic, population
* `NH_ASIAN10`: Asian, non-hispanic, population
* `NH_NHPI10`: Native Hawaiian and Pacific Islander, non-hispanic, population
* `NH_OTHER10`: Other race, non-hispanic, population
* `NH_2MORE10`: Two or more races, non-hispanic, population
* `HISP10`: Hispanic population
* `H_WHITE10`: White, hispanic, population
* `H_BLACK10`: Black, hispanic, population
* `H_AMIN10`: American Indian and Alaska Native, hispanic, population
* `H_ASIAN10`: Asian, hispanic, population
* `H_NHPI10`: Native Hawaiian and Pacific Islander, hispanic, population
* `H_OTHER10`: Other race, hispanic, population
* `H_2MORE10`: Two or more races, hispanic, population
* `VAP19`: Total voting age population

## Projection
This shapefile uses a NAD83(Harn)/UTM zone 17 North projection (EPSG:3747).
