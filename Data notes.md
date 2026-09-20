# Data notes



## GRID3 Nigeria Operational LGAs v3.0

- Source: https://data.grid3.org

Downloaded: 9/13/2026

- 774 features, polygons

- Columns: FID(Integer (64 bit)), globalid(Text (string)), uniq\_id(Integer (32 bit)), timestamp(Date & Time), editor(Text (string)), Iganame(Text (string)), Igacode(Text (string)), statename(Text (string)), statecode(Text (string)), source(Text (string)), amapcode(Text (string).

- No nulls in lga\_name

- Covers my LGA fully


## OSM amenities, extracted via QuickOSM

- Query: amenities in Katsina

- Extracted: 9/13/2026

- 69 features (points)

- Some values of the name field are null, and some additional fields contain null values for more than 80% of the attributes

- Coverage looks good in the built-up area and is not sparse at the edges; only a few are.


## CRS and preparation
- All source layers arrived in EPSG:4326
- Study area: Dutsi, extracted from GRID3 LGAs
### All layers clipped to study area, then reprojected to EPSG:32632 (UTM 32N)
- Area check: Dutsi LGA 370 km2, matches published figure
- Working files in data/processed/, raw files untouched



- I reprojected my LGA, which is Dutsi LGA, from the GRID3 LGAs data; it was in 4326 before it was reprojected to UTM 32632 (32) because Katsina is around eastend nd central parts of the country. I initially got null across all rows for the area field, but after it was reprojected, it worked. 
