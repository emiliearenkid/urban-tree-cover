# urban-tree-cover
Final project for LIS 545: Data Curation during the Winter 2022 Quarter. It contains three different datasets from U.S. City's Open Data platforms.


Street_Tree_List from San Francisco, CA downloaded from https://data.sfgov.org/City-Infrastructure/Street-Tree-List/tkzw-k3nq

Urban_Forestry_Street_Trees from Washington, DC downloaded from https://opendata.dc.gov/datasets/DCGIS::urban-forestry-street-trees/about

Tree_Inventory from Austin, Texas downloaded from https://data.austintexas.gov/Locations-and-Maps/Tree-Inventory/wrik-xasw

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
        - Even though the Citrus spp. tree would separate to create three Common Names columns, I decided the value gained from this distinction was not important to my users.
- Austin, TX
    - Separated Geometry into X and Y columns.
    - Renamed New Georeferenced Column to GEOJSON_COORDINATES.
    - Rmoved the GEOMETRY column because it is a field output unique to GIS that has no use for my users.
    - Renamed the X and Y columns to SPECIFIC_LONGITUDE and SPECIFIC_LATITUDE, respectively.
    - Renamed SPECIES to COMMON_NAME.
    - Renamed DIAMETER to DBH.
Version 2.0 of all datasets is turning them back into csvs for upload to GitHub.

Data Dictionary: 

Washington D.C.
    X: None
    Y: None
    OBJECTID: Internal feature number that are automatically sequentially generated. Sourced from ESRI. 
    FACILITYID: Unique tree identifier. Sourced from District of Columbia, Department of Transportation, Urban Forestry Administration. 
    VICINITY: Address in immediate vicinity of the tree. Sourced from District of Columbia, Department of Transportation, Urban Forestry Administration. 
    WARD: Ward. Sourced from District of Columbia, Department of Transportation.
    TBOX_L: Tree box length. Sourced from District of Columbia, Department of Transportation, Urban Forestry Administration. 
    TBOX_W: Tree box width. Sourced from District of Columbia, Department of Transportation, Urban Forestry Administration. 
    WIRES: Overhead electrical wires. Sourced from District of Columbia, Department of Transportation, Urban Forestry Administration. 
    CURB: Curb type. Sourced from District of Columbia, Department of Transportation, Urban Forestry Administration. 
    SIDEWALK: Sidewalk type. Sourced from District of Columbia, Department of Transportation, Urban Forestry Administration. 
    TBOX_STAT: Plantable status of location. Sourced from District of Columbia, Department of Transportation, Urban Forestry Administration. 
    RETIREDDT: Date of location retirement. Sourced from District of Columbia, Department of Transportation, Urban Forestry Administration. 
    SCI_NM: Scientific name. Sourced from District of Columbia, Department of Transportation, Urban Forestry Administration. 
    CCMN_NM: Common name. Sourced from District of Columbia, Department of Transportation, Urban Forestry Administration. 
    DATE_PLANT: Mosst recent planting date of location. Sourced from District of Columbia, Department of Transportation, Urban Forestry Administration. 
    DBH: Diameter at breast height. Commonly measured at 4.5 ft from the soil surface. Sourced from District of Columbia, Department of Transportation, Urban Forestry Administration. 
    DISEASE: Observation of tree disease incidence. Sourced from District of Columbia, Department of Transportation, Urban Forestry Administration. 
    PESTS: Observation of tree pest incidence. Sourced from District of Columbia, Department of Transportation, Urban Forestry Administration. 
    CONDITION: Generalized tree health via visual inspection. Sourced from District of Columbia, Department of Transportation, Urban Forestry Administration. 
    CONDITIODT: Most recent date of condition inspection. Sourced from District of Columbia, Department of Transportation, Urban Forestry Administration. 
    OWNERSHIP: Ownership of tree. Sourced from District of Columbia, Department of Transportation, Urban Forestry Administration. 
    TREE_NOTES: Comments. Sourced from District of Columbia, Department of Transportation, Urban Forestry Administration. 
    ONEYEARPHOTO: None. Sourced from District of Columbia, Department of Transportation, Urban Forestry Administration. 
    SPECIALPHOTO: None. Sourced from District of Columbia, Department of Transportation, Urban Forestry Administration. 
    PHOTOREMARKS: None. Sourced from District of Columbia, Department of Transportation, Urban Forestry Administration. 
    ELEVATION: Level of soil at base of tree or in tree box. Sourced from District of Columbia, Department of Transportation, Urban Forestry Administration. 
    SIGN: Type of sign in close proximity to tree. Sourced from District of Columbia, Department of Transportation, Urban Forestry Administration. 
    TRRS: None. Sourced from District of Columbia, Department of Transportation, Urban Forestry Administration. 
    WARRANTY: Planting season when plant warranty began. Sourced from District of Columbia, Department of Transportation, Urban Forestry Administration. 
    FAM_NAME: None.
    CREATED_USER: None.
    CREATED_DATE: None.
    EDITEDBY: None.
    LAST_EDITED_USER: None.
    LAST_EDITED_DATE: None.
    GENUS_NAME: None.
    GIS_ID: None.
    GLOBALID: None.
    CREATOR: None.
    CREATED: None.
    EDITOR: None.
    EDITED: None.
    MBG_WIDTH: None.
    MBG_LENGTH: None.
    MBG_ORIENTATION: None.
    MAX_CROWN_HEIGHT: None.
    MAX_MEAN: None.
    MIN_CROWN_BASE: None.
    DTM_MEAN: None.
    PERIM: None.
    CROWN_AREA: None.
    CICADA_SURVEY: None.
    SHAPE: Feature geometry. Sourced from ESRI.

San Francisco, CA
    TreeID: Number. Unique ID of tree.
    qLegalState: Text. Legal status: either "Permitted" or "DPW maintained".
    qSpecies: Text. Species of tree.
    qAddress: Text. Address of tree.
    SiteOrder: Number. Order of tree at address where multiple trees are at the same address. Trees are ordered in ascending address order. 
    qSiteInfo: Text. Description of the location of the tree.
    PlantType: Text. Either "Landscaping" or "Tree".
    qCaretaker: Text. Agency or person that is primary caregiver to the tree. The owner of the tree.
    qCareAssistant: Text. Agency or person that is secondary caregiver to the tree.
    PlantDate: Date. Date the tree was planted.
    DBH: Text. Diameter at Breast Height.
    PlotSize: Text. Dimension of tree plot.
    PermitNotes: Text. Tree permit number reference.
    xCoord: Number. CA State Plane III.
    yCoord: Number. CA State Plane III.
    Latitude: Number. WGS84.
    Longitude: Number. WGS84.
    Location: Location. Location formatted for mapping.
    Fire Prevention District: None.
    Police Districe: None.
    Supervisor District: None.
    Zipcodes: None.
    Neighborhoods (old): None.
    Analysis Neighborhoods: None.

Austin, TX
    Geometry: Point. Feature's geometry type. This fields is generated from the GIS platform.
    X: Number. The first number contained in the Geometry field.
    Y: Number. The second number contained in the Geometry field.
    Species: Text. Common species name of the tree.
    Diameter: Number. Diameter of the tree at Breast Height (4.5ft from the ground). Units in inches.
    Latitude: Number. Estimated latitude of tree location.
    Longitude: Number. Estimated longitude of tree column.
    New Georeferenced Column: Point in GeoJSON format.

Metadata (Project Open Data's DCAT-US Metadata Schema)
Attribute           Value
-----------------------------------------------------------------------------
conformsTo          URI that identifies the version of the schema being used.
dataset             A container for the array of Dataset objects.
title               Human-readable context-inclusive name of the asset
description         Human-readable context-inclusive description (abstract) of the asset
keyword             Tags/keywords to help users (technical+non-technical) discover your dataset
modified            Most recent date on which the dataset was changed, updated or modified.
publisher           The publishing entity and optionally their parent organization(s). Is a group of fields to be expanded on
contactPoint        Contact person’s name and email for the asset.
identifier          A unique identifier for the dataset or API as maintained within an Agency catalog or database.
accessLevel         The degree to which this dataset could be made publicly-available, regardless of whether it has been made available. Choices: public (Data asset is or could be made publicly available to all without restrictions), restricted public (Data asset is available under certain use restrictions), or non-public (Data asset is not available to members of the public).
license              	The license or non-license (i.e. Public Domain) status with which the dataset or API has been published. See Open Licenses for more information.
describedBy         URL to the data dictionary for the dataset. Note that documentation other than a data dictionary can be referenced using Related Documents (references).
describedByType     The machine-readable file format (IANA Media Type also known as MIME Type) of the dataset’s Data Dictionary (describedBy).
isPartOf            The collection of which the dataset is a subset.
language            The language of the dataset.
landingPage         This field is not intended for an agency’s homepage (e.g. www.agency.gov), but rather if a dataset has a human-friendly hub or landing page that users can be directed to for all resources tied to the dataset.
accessURL           URL providing indirect access to a dataset, for example via API or a graphical interface.
format              A human-readable description of the file format of a distribution.

WASHINGTON D.C.
Attribute           Value
-----------------------------------------------------------------------------
conformsTo          https://project-open-data.cio.gov/v1.1/schema
title               Urban Forestry Washington D.C. Street Trees
description         This dataset contains trees and tree locations managed by the Urban Forestry Administration (UFA) in the District of Columbia. The dataset contains locations and attributes of Trees created as part of Department of Transportation (DDOT) Street Spatial Database (SSD).
keyword             "trees", "urban tree cover", "urban canopy", "tree canopy", "street trees", "city trees"
modified            2023-03-06
publisher           Emilie Hoy
fn                  Emilie Hoy
hasEmail            hoye@uw.edu
accessLevel         public
describedBy         https://github.com/emiliearenkid/urban-tree-cover
describedByType     .md
language            en-US
references          https://opendata.dc.gov/datasets/DCGIS::urban-forestry-street-trees/about
landingPage         https://github.com/emiliearenkid/urban-tree-cover
accessURL           https://github.com/emiliearenkid/urban-tree-cover
format              CSV
downloadURL         TO BE ADDED
mediaType           CSV

SAN FRANCISCO, CA
Attribute           Value
conformsTo          https://project-open-data.cio.gov/v1.1/schema
title               San Francisco Street Tree List
description         This dataset contains trees and tree locations managed by the San Francisco Department of Public Works. The dataset contains locations and attributes of Trees including planting date and species.
keyword             "trees", "urban tree cover", "urban canopy", "tree canopy", "street trees", "city trees"
modified            2023-03-06
publisher           Emilie Hoy
fn                  Emilie Hoy
hasEmail            hoye@uw.edu
accessLevel         public
describedBy         https://github.com/emiliearenkid/urban-tree-cover
describedByType     .md
language            en-US
references          https://data.sfgov.org/City-Infrastructure/Street-Tree-List/tkzw-k3nq
landingPage         https://github.com/emiliearenkid/urban-tree-cover
accessURL           https://github.com/emiliearenkid/urban-tree-cover
format              CSV
downloadURL         TO BE ADDED
mediaType           CSV

AUSTIN, TX
Attribute           Value
-----------------------------------------------------------------------------
conformsTo          https://project-open-data.cio.gov/v1.1/schema
title               Tree Inventory Austin Texas
description         This dataset contains trees and tree locations inventoried by the City of Austin as of March 13th, 2020. Data came from many sources including the Development Services Department's Tree Division, AISD, Parks and Recreation Department, and Public Works Department's downtown tree inventory (2013). The City admits some errors and duplicates may exist in the dataset.
keyword             "trees", "urban tree cover", "urban canopy", "tree canopy", "street trees", "city trees"
modified            2023-03-06
publisher           Emilie Hoy
fn                  Emilie Hoy
hasEmail            hoye@uw.edu
accessLevel         public
describedBy         https://github.com/emiliearenkid/urban-tree-cover
describedByType     .md
language            en-US
references          https://data.austintexas.gov/Locations-and-Maps/Tree-Inventory/wrik-xasw
landingPage         https://github.com/emiliearenkid/urban-tree-cover
accessURL           https://github.com/emiliearenkid/urban-tree-cover
format              CSV
downloadURL         TO BE ADDED
mediaType           CSV

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