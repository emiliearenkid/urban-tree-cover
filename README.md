# README.md
Final project for LIS 545: Data Curation during the Winter 2022 Quarter. It contains three different datasets from U.S. City's Open Data platforms. Each dataset uses the original name separated by underscores with the city it came from appended to the end.
## Table of Contents
- [Edits and Standardization](https://github.com/emiliearenkid/urban-tree-cover/edit/main/README.md#edits-and-standardization)
- [Data Dictionary](https://github.com/emiliearenkid/urban-tree-cover/edit/main/README.md#data-dictionary)
- [Metadata](https://github.com/emiliearenkid/urban-tree-cover/edit/main/README.md#metadata)
- [Rights](https://github.com/emiliearenkid/urban-tree-cover/edit/main/README.md#rights)
- [Contact](https://github.com/emiliearenkid/urban-tree-cover/edit/main/README.md#contact)
## Edits and Standardization
Changes made to Datasets: 
Version 1 of all datasets is transforming them to Excel sheets for easier modification.
Version 1.1 of all datasets includes the following edits to make them compatible for analysis.
- Washington D.C.
    - Renamed FACILITYID column to TREEID.
    - Delete OBJECTID column because it is only used as an internal number (meaningless without the internal context).
    - Added LOCATION column to combine X and Y values.
    - Changed X column to LONGITUDE and Y column to LATITUDE.
    - Removed the Cicada_Survey, Shape, Disease, Pests, Ownership, OneYearPhoto, SpecialPhoto, PhotoRemarks, Elevation, Sign, TRRS, Warranty, Created_User, Created_Date, GIS_ID, GlobalID, Creator, Created, Editor, Edited, TBox_Stat, Sidewalk, Curb, Wires, TBox_Width, TBox_Length, Ward, Condition, ConditioDT, EditedBy, Last_Edited_User, and RetireDDT columns.
    - Moved the FAM_NAME and GENUS_Name columns next to each other and moved the LAST_EDITED_DATE to the last column.
    - Removed the MBG_WIDTH, MBG_LENGTH, MBG_ORIENTATION, MAX_CROWN_HEIGHT, MAX_MEAN, MIN_CROWN_BASE, DTM_MEAN, PERIM, and CROWN_AREA columns.
    - Removed the TREE_NOTES and DATE_PLANT columns. 
    - Added a GEOJSON_CORDINATES column, like the Austin, TX dataset to have a field with a GeoJSON Point data type for ease with importing into GIS.
    - Removed the FAM_NM and GENUS_NM fields.
    - Changes the SCI_NM and CMMN_NM fields to SCIENTIFIC_NAME and COMMON_NAME, respectfully.
- San Francisco, CA
    - Capitalized all columns.
    - Added a GEOJSON_CORDINATES column, like the Austin, TX dataset to have a field with a GeoJSON Point data type for ease with importing into GIS programs.
    - Removed the FIREPREVENTIONDISTRICT, POLICEDISTRICT, SUPERVISORDISTRICT, ZIPCODES, NEIGHBORHOODS(OLD), AND ANALYSISNEIGHBORHOODS fields.
    - Removed the PLOTSIZE, PERMITNOTES, XCOORD, and YCOORD fields.
    - Removed the QLEGALSTATE, SITEORDER, QSITEINFO, PLANTTYPE, QCARETAKER, QCAREASSISTANT, and PLANTDATE fields.
    - Separate the "SPECIES" field into SCIENTIFIC_NAME, COMMON_NAME, and COMMON_NAME2.
- Austin, TX
    - Separated Geometry into X and Y columns.
    - Renamed New Georeferenced Column to GEOJSON_COORDINATES.
    - Rmoved the GEOMETRY column because it is a field output unique to GIS that has no use for my users.
    - Renamed the X and Y columns to SPECIFIC_LONGITUDE and SPECIFIC_LATITUDE, respectively.
    - Renamed SPECIES to COMMON_NAME.
    - Renamed DIAMETER to DBH.
Version 1.2 of all datasets is turning them back into csvs for upload to GitHub.
## Data Dictionary
**WASHINGTON D.C.**
| Variable | Label | Type | Allowed Values | Description |
|----------------|-----------|-----|-------------------------------|-------------------------------------------|
| Latitude | LATITUDE | double | positive or negative number | The estimated latitutde of the tree's location. |
| Longitude | LONGITUDE | double | positive or negative number | The estimated longitude of the tree's location. |
| Coordinates | LOCATION | Coordinates | latitude, longitude pair | The approximate coordinates of the tree's location. |
| GIS Coordinates | GEOJSON_COORDINATES | GeoJSON Point | longitude, latitude pair | Coordinates field with latitude and longitude values switches for ease of GIS mapping. |
| Unique Identifier | TREEID | int | Unique positive whole numbers | Unique tree identifier. Sourced from District of Columbia, Department of Transportation, Urban Forestry Administration. |
| Address | VICINITY | string | N/A | Address in immediate vicinity of the tree. Sourced from District of Columbia, Department of Transportation, Urban Forestry Administration. |
| Scientific Name | SCIENTIFIC_NAME | string | N/A | Scientific name. Sourced from District of Columbia, Department of Transportation, Urban Forestry Administration. |
| Common Tree Name | COMMON_NAME | string | N/A | Common name. Sourced from District of Columbia, Department of Transportation, Urban Forestry Administration. |
| Diameter Breast Height | DBH | float | N/A | Diameter at breast height. Commonly measured at 4.5 ft from the soil surface. Sourced from District of Columbia, Department of Transportation, Urban Forestry Administration. |
| Last Edited | LAST_EDITED_DATE | date | N/A | Last time this tree's data was updated. |

**SAN FRANCISCO, CA**
| Variable | Label | Type | Allowed Values | Description |
|----------------|-----------|-----|-------------------------------|-------------------------------------------|
| Unique Identifier | TREEID | int | Unique positive whole numbers | Unique ID of tree. |
| Scientific Name | SCIENTIFIC_NAME | string | N/A | The scientific name of the tree. |
| Common Name | COMMON_NAME | string | N/A | The common name of the tree. |
| Common Name Extended | COMMON_NAME2 | string | N/A | Alternate common names or specific strains of a well known tree. |
| Address | LOCATION | string | N/A | Address the tree is located at. |
| Diameter Breast Height | DBH | float | Any positive or negative float | Diameter at breast height. Commonly measured at 4.5 ft from the soil surface. |
| Latitude | LATITUDE | double | positive or negative number | WGS84 format latitude coordinates. |
| Longitude | LONGITUDE | double | positive or negative number | WGS84 format longitude coordinates. |
| Coordinates | LOCATION | Coordinates | latitude, longitude pair | Location formatted for mapping. |
| GIS Coordinates | GEOJSON_COORDINATES | GEOJSON Point | longitude, latitude pair | Coordinates field with latitude and longitude values switches for ease of GIS mapping. |

**AUSTIN, TX**
| Variable | Label | Type | Allowed Values | Description |
|----------------|-----------|-----|-------------------------------|-------------------------------------------|
| GIS Longitude | SPECIFIC_LONGITUDE | double | positive or negative number | The estimated longitude of the tree's location. Retrieved from GIS map. |
| GIS Latitude | SPECIFIC_LATITUDE | double | positive or negative number | The estimated latitutde of the tree's location. Retrieved from GIS map. |
| Common Name | COMMON_NAME | string | N/A | The common name of the tree. |
| Diameter Breast Height | DBH | float | Any positive or negative float | Diameter at breast height. Commonly measured at 4.5 ft from the soil surface. |
| Latitude | LATITUDE | double | positive or negative number | The estimated latitude of the tree's location. |
| Longitude | LONGITUDE | double | positive or negative number | The estimated longitude of the tree's location. |
| GIS Coordinates | GEOJSON_COORDINATES | GEOJSON Point | longitude, latitude pair | Coordinates field with latitude and longitude values switches for ease of GIS mapping. |
## Metadata
**WASHINGTON D.C.**
| Attribute | Value         |
|-------------------|---------------|
| conformsTo | [https://project-open-data.cio.gov/v1.1/schema](https://project-open-data.cio.gov/v1.1/schema) |
| title | Urban Forestry Washington D.C. Street Trees |
| description | This dataset contains trees and tree locations managed by the Urban Forestry Administration (UFA) in the District of Columbia. The dataset contains locations and attributes of Trees created as part of Department of Transportation (DDOT) Street Spatial Database (SSD). |
| keyword | "trees", "urban tree cover", "urban canopy", "tree canopy", "street trees", "city trees" |
| modified | 2023-03-06 |
| publisher | Emilie Hoy |
| fn | Emilie Hoy |
| hasEmail | hoye@uw.edu |
| accessLevel | public |
| describedBy | [https://github.com/emiliearenkid/urban-tree-cover](https://github.com/emiliearenkid/urban-tree-cover) |
| describedByType | .md |
| language | en-US |
| references | [https://opendata.dc.gov/datasets/DCGIS::urban-forestry-street-trees/about](https://opendata.dc.gov/datasets/DCGIS::urban-forestry-street-trees/about) |
| landingPage | [https://github.com/emiliearenkid/urban-tree-cover](https://github.com/emiliearenkid/urban-tree-cover) |
| accessURL | [https://github.com/emiliearenkid/urban-tree-cover](https://github.com/emiliearenkid/urban-tree-cover) |
| format | CSV |
| downloadURL | TO BE ADDED |
| mediaType | CSV |

**SAN FRANCISCO, CA**
| Attribute | Value         |
|-------------------|---------------|
| conformsTo | [https://project-open-data.cio.gov/v1.1/schema](https://project-open-data.cio.gov/v1.1/schema) |
| title | San Francisco Street Tree List |
| description | This dataset contains trees and tree locations managed by the San Francisco Department of Public Works. The dataset contains locations and attributes of Trees including planting date and species. |
| keyword | "trees", "urban tree cover", "urban canopy", "tree canopy", "street trees", "city trees" |
| modified | 2023-03-06 |
| publisher | Emilie Hoy |
| fn | Emilie Hoy |
| hasEmail | hoye@uw.edu |
| accessLevel | public |
| describedBy | [https://github.com/emiliearenkid/urban-tree-cover](https://github.com/emiliearenkid/urban-tree-cover) |
| describedByType | .md |
| language | en-US |
| references | [https://data.sfgov.org/City-Infrastructure/Street-Tree-List/tkzw-k3nq](https://data.sfgov.org/City-Infrastructure/Street-Tree-List/tkzw-k3nq) |
| landingPage | [https://github.com/emiliearenkid/urban-tree-cover](https://github.com/emiliearenkid/urban-tree-cover) |
| accessURL | [https://github.com/emiliearenkid/urban-tree-cover](https://github.com/emiliearenkid/urban-tree-cover) |
| format | CSV |
| downloadURL | TO BE ADDED |
| mediaType | CSV |

**AUSTIN, TX**
| Attribute | Value         |
|-------------------|---------------|
| conformsTo | [https://project-open-data.cio.gov/v1.1/schema](https://project-open-data.cio.gov/v1.1/schema) |
| title | Tree Inventory Austin Texas |
| description | This dataset contains trees and tree locations inventoried by the City of Austin as of March 13th, 2020. Data came from many sources including the Development Services Department's Tree Division, AISD, Parks and Recreation Department, and Public Works Department's downtown tree inventory (2013). The City admits some errors and duplicates may exist in the dataset. |
| keyword | "trees", "urban tree cover", "urban canopy", "tree canopy", "street trees", "city trees" |
| modified | 2023-03-06 |
| publisher | Emilie Hoy |
| fn | Emilie Hoy |
| hasEmail | hoye@uw.edu |
| accessLevel | public |
| describedBy | [https://github.com/emiliearenkid/urban-tree-cover](https://github.com/emiliearenkid/urban-tree-cover) |
| describedByType | .md |
| language | en-US |
| references | [https://data.austintexas.gov/Locations-and-Maps/Tree-Inventory/wrik-xasw](https://data.austintexas.gov/Locations-and-Maps/Tree-Inventory/wrik-xasw) |
| landingPage | [https://github.com/emiliearenkid/urban-tree-cover](https://github.com/emiliearenkid/urban-tree-cover) |
| accessURL | [https://github.com/emiliearenkid/urban-tree-cover](https://github.com/emiliearenkid/urban-tree-cover) |
| format | CSV |
| downloadURL | TO BE ADDED |
| mediaType | CSV |
## Rights
These curated datasets are freely available for use and reuse by anyone.
Each of the datasets were modified from the three open data platforms below. 
- Street_Tree_List from San Francisco, CA downloaded from https://data.sfgov.org/City-Infrastructure/Street-Tree-List/tkzw-k3nq
- Urban_Forestry_Street_Trees from Washington, DC downloaded from https://opendata.dc.gov/datasets/DCGIS::urban-forestry-street-trees/about
- Tree_Inventory from Austin, Texas downloaded from https://data.austintexas.gov/Locations-and-Maps/Tree-Inventory/wrik-xasw
## Contact
hoye@uw.edu
