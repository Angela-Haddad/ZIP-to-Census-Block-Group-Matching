# ZIP-to-Census-Block-Group-Matching
This project includes a csv file to match zip codes with corresponding Census Block Groups (CBG)and identifying the percentage of overlap in their areas.

A census block group is a set of one or more contiguous census blocks. The block group geography is the smallest geographic area for which American Community Survey data. However, it is not possible to perform 1-1 matching between CBGs and ZIP codes since they were delineated differently. The figure below, for example, shows that the ZIP (red boundary) completely contains some CBGs (light grey polygons with a black outline) but only partially overlaps other CBGs. 

![example](https://user-images.githubusercontent.com/89271368/214699725-f161865b-186f-4d16-8c61-009c2f3026d9.PNG)

This dataset includes matching CBGs with ZIP codes based on the Census 2020 boundaries. 

Below is the description of each column:

* OBJECTID: arbitrary ID for a polygon the presents an intersection between a CBG and a ZIP
* ZCTA5: the ZIP code
* StateFIPS: the Federal Information Processing System Codes for States
* CountyFIPS: the Federal Information Processing System Codes for Counties 
* TractCode: 	a 4-digit code corresponding to Tracts within a county
* BlockGroup: a 1-digit code corresponding to a block groups within a tract 
* CensusBlockGroup: a	12 characters unique code corresponding to a CBG. It combines the state FIPS code, county FIPS code, tract code, and block group number.
* State: the full name of the state in letters	
* County: the full name of the county	in letters
* Percent_Overlap: the percentage of the CBG are that is within a ZIP code. For example, a value of 1 means that the CBG is completely within the ZIP, while a value of 0.25 means that 25% of the block group is located within the ZIP.

