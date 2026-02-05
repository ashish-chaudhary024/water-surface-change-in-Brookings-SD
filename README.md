# Temporal Change in Open Water Surface (2013–2025): Brookings County, SD

## Overview
This repository contains the final project for the *Agricultural Remote Sensing* course.  
The study analyzes temporal changes in open water surface area in Brookings County, South Dakota, from 2013 to 2025 using Landsat imagery and the Normalized Difference Water Index (NDWI).

Open water is an important environmental indicator reflecting rainfall, snowmelt, drought conditions, land-use change, and climate variability. Due to the lack of recent official statistics, satellite data were used to assess annual surface water changes.

---

## Study Area
- **Location:** Brookings County, South Dakota, USA  
- **Reference water area (2012, U.S. Census):** 12.7 sq. miles (~33 km²)

---

## Data
- **Satellite:** Landsat 8 & Landsat 9  
- **Source:** USGS EarthExplorer (https://earthexplorer.usgs.gov)  
- **Time period:** 2013–2025  
- **Spatial resolution:** 30 m × 30 m  

### Image Selection
- Priority given to **July** images (dry season)  
- **June** images used when July was cloudy  
- **May** images used for 2018, 2019, and 2021 due to cloud cover  

---

## Methodology
1. Landsat digital numbers were converted to Top of Atmosphere (TOA) reflectance:  
Reflectance = (DN × 0.0000075) − 0.2
2. NDWI was calculated using McFeeters (1996):

    NDWI = (Green − NIR) / (Green + NIR)

- Green: Band 3  
- NIR: Band 5  

3. Brookings County boundary was applied using **Extract by Mask** in ArcGIS Pro.  
4. NDWI maps were reclassified into **water** and **non-water** using a threshold of **−0.1**.  
5. Open water area was calculated using pixel count and Landsat resolution (30 m × 30 m).

---

## Results
- Surface water area fluctuated annually from 2013 to 2025.  
- Large water bodies (e.g., Big Sioux River) remained relatively stable.  
- Smaller water bodies showed noticeable variation.  
- The highest water extent occurred in **2019** due to flooding.  
- The lowest surface water area was observed in **2023 and 2024** (below 30 km²).  
- Overall, surface water area increased compared to the 2012 baseline.

---

## Repository Contents
├── PPT/ # Final presentation  
├── NDWI_Maps/ # NDWI outputs (2013–2025)  
├── Classified_Maps/ # Water / Non-water maps  
├── Videos/ # NDWI temporal change animation  
├── Shapefile/ # Brookings County boundary  
└── README.md  


---

## Key Takeaways
- NDWI is effective for mapping open water surfaces.  
- Surface water in Brookings County shows strong interannual variability.  
- This workflow is reproducible and applicable to other regions.  
- Results are useful for hydrology and land management planning.

---

## Reference
McFeeters, S. K. (1996). *The use of the Normalized Difference Water Index (NDWI) in the delineation of open water features*. International Journal of Remote Sensing.

