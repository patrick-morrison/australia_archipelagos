# The evolution of island geographies and the emergence and persistence of Indigenous maritime cultures
Patrick Morrison 7th of February 2023
This notebook contains the analysis run for 'The evolution of island geographies and the emergence and persistence of Indigenous maritime cultures' (Morrison et al 2023.)

## R code files
### archaeological-dates-for-island-occupation-in-australia.Rmd
This file contains the code for organising and plotting island radiocarbon dates by region.
### evolution-of-islands-in-australia.Rmd
This file contains the code for the GIS analysis of islands throughout time. Note this is quite resource intensive, and will take several hours to run. Inf you want to speed it up, uncomment the aggregate command on line 54 to downscale the bathymetry. 

## external data:
The code requires the external data folder containing:
- geodata_coast/: http://pid.geoscience.gov.au/dataset/ga/61395
- sahularch_c14/: SahulArch Radiocarbon Collection v.2: https://zenodo.org/record/7160945#.Y-C0hnZBwuU
- Austarch_1-3_and_IDASQ_28Nov13-1.csv: https://doi.org/10.5284/1027216
- grant2012.xls: Supplemtary data of https://doi.org/10.1038/nature11593
- IBRA7_regions/: The Interim Biogeographic Regionalisation for Australia (IBRA), Version 7 (Regions)https://www.environment.gov.au/fed/catalog/search/resource/details.page?uuid=%7B4A2321F0-DD57-454E-BE34-6FD4BDE64703%7D
- ausbath/: https://data.gov.au/data/dataset/australian-bathymetry-and-topography-grid-june-2009
- imcra_mesoscale_bioregions:/ Marine bioregions for QGIS project: https://data.gov.au/data/dataset/4-integrated-marine-and-coastal-regionalisation-of-australia-imcra-v4-0-meso-scale-bioregions

## inputs
The inputs provided are:
- additional_dates.csv: some additional radiocarbon dates mentioned in the paper
- islands_austarch.csv: A lookup table of sites to assign correct island
- lake_eyre.geojson: boundaries to exclude lake eyre
- references.bib: references for the rmarkdown files
- regions.geojson: analytical regions used for timeseries
- pois.geojson: points of interest used in the detailed mapping

## output_dates
these are the outputs of archaeological-dates-for-island-occupation-in-australia.Rmd
- dates_database.png: showing all dates used
- dates_timeseries.png: showing the time series figure

## output_islands
these are the outputs of evolution-of-islands-in-australia.Rmd
- area/: island area graphs for every 2ka
- data/: regional summaries for every 2ka
- intervis:/ intervisibility surface graphs for every 2ka
- pub/: files for publication figures
    - sea_levels.png used as-is in publication
    - folders containing the output for the 4 different sea levels, including the pdfs that were used to produce the main figure
- spatial:/ spatial data for every 2ka

## interpretation
Non-code files for producing figures
- australian_archipelagos.qgs - QGIS project for producing maps
- islands_summary_graph.afdesign - Affinity designed amalgamation of sea stand pdf outputs
- maps/: maps exported from QGIS