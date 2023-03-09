# README.md
Final project for LIS 545: Data Curation during the Winter 2022 Quarter. It contains three different datasets from U.S. City's Open Data platforms.
## Table of Contents
- [Edits and Standardization](https://github.com/emiliearenkid/urban-tree-cover/edit/main/README.md#edits-and-standardization)
- [Data Dictionary](https://github.com/emiliearenkid/urban-tree-cover/edit/main/README.md#data-dictionary)
- [Metadata](https://github.com/emiliearenkid/urban-tree-cover/edit/main/README.md#metadata)
- [Rights](https://github.com/emiliearenkid/urban-tree-cover/edit/main/README.md#rights)
- [Contact](https://github.com/emiliearenkid/urban-tree-cover/edit/main/README.md#contact)
## Edits and Standardization
## Data Dictionary
**WASHINGTON D.C.**
| Variable | Label | Type | Allowed Values | Description |
|----------------|-----------|-----|-------------------------------|-------------------------------------------|
| Latitude | LATITUDE | double | positive or negative number | The estimated latitutde of the tree's location. |
| Longitude | LONGITUDE | double | positive or negative number | The estimated longitude of the tree's location. |
| Coordinates | LOCATION | Coordinates | latitude, longitude pair | The approximate coordinates of the tree's location. |
| GIS Coordinates | GEOJSON_COORDINATES | GeoJSON | longitude, latitude pair | Coordinates field with latitude and longitude values switches for ease of GIS mapping. |
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
| GIS Coordinates | GEOJSON_COORDINATES | GEOJSON | longitude, latitude pair | Coordinates field with latitude and longitude values switches for ease of GIS mapping. |

**AUSTIN, TX**
| Variable | Label | Type | Allowed Values | Description |
|----------------|-----------|-----|-------------------------------|-------------------------------------------|
| GIS Longitude | SPECIFIC_LONGITUDE | double | positive or negative number | The estimated longitude of the tree's location. Retrieved from GIS map. |
| GIS Latitude | SPECIFIC_LATITUDE | double | positive or negative number | The estimated latitutde of the tree's location. Retrieved from GIS map. |
| Common Name | COMMON_NAME | string | N/A | The common name of the tree. |
| Diameter Breast Height | DBH | float | Any positive or negative float | Diameter at breast height. Commonly measured at 4.5 ft from the soil surface. |
| Latitude | LATITUDE | double | positive or negative number | The estimated latitude of the tree's location. |
| Longitude | LONGITUDE | double | positive or negative number | The estimated longitude of the tree's location. |
| GIS Coordinates | GEOJSON_COORDINATES | GEOJSON | longitude, latitude pair | Coordinates field with latitude and longitude values switches for ease of GIS mapping. |
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
