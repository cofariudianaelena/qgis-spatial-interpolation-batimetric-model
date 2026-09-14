# Spatial Interpolation & Batimetric DTM Generation in QGIS

## Overview
This repository contains two practical GIS laboratory projects focused on **spatial data interpolation, Digital Terrain Model (DTM) generation, and bathymetric mapping** using **QGIS**. The workflows cover point data processing, TIN and IDW interpolation techniques, raster clipping via polygon masks, and automated vector contour extraction[cite: 3].

---

## Technical Specifications
* **Software:** QGIS (Open Source GIS)[cite: 3]
* **Coordinate Reference Systems:** 
  * Dealul Piscului 1970 / Stereo 70 (EPSG:31700)[cite: 3]
  * NAD83 / Texas North Central (EPSG:2276)[cite: 3]
* **Input Datasets:** 
  * 30 discrete topographic elevation points (`.csv`)[cite: 3]
  * Large-scale bathymetric survey dataset for Lake Martin, Texas (over 270,000 depth points, lake boundary polygons, and island layers)[cite: 3]

---

## Project Methodology & Workflows

### Project 1: Surface Modeling & Spatial Interpolation (Small Dataset)
* **Data Ingestion & CRS Setup:** Imported 3D point data from CSV files and configured the project workspace to the **Stereo 70** projection system[cite: 3].
* **Vector Conversion:** Exported point coordinates into an ESRI Shapefile format retaining Z-dimension properties[cite: 3].
* **TIN Interpolation:** Generated a Triangular Irregular Network (Delaunay triangulation) and converted it into a continuous raster surface with a 100-meter cell resolution[cite: 3].
* **IDW Interpolation:** Applied Inverse Distance Weighted interpolation (with a distance coefficient $P=9$) to evaluate spatial transition behaviors[cite: 3].
* **Comparative Symbology:** Visualized both models using continuous spectral color ramps to analyze elevation variances[cite: 3].

### Project 2: Advanced Bathymetric Mapping & Contour Extraction (Lake Martin)
* **Large Dataset Management:** Processed over 270,000 acoustic depth soundings collected via DGPS (`Martin_pts.shp`)[cite: 3].
* **Boundary Masking:** Incorporated lake polygon boundaries (`Martin_lk_poly.shp`) and island layers to constrain interpolation limits[cite: 3].
* **Raster Clipping:** Applied GDAL mask extraction tools (`Clip raster by mask layer`) to isolate bathymetric surfaces within the lake limits[cite: 3].
* **Contour Generation:** Extracted vector contour lines at defined intervals (10-foot spacing) directly from the clipped raster grid[cite: 3].
* **Advanced Labeling:** Configured curved vector label placements to display precise elevation/depth values along contour lines[cite: 3].

---

## Deliverables
* Interpolated TIN and IDW elevation rasters (`.tif`)[cite: 3]
* Clipped bathymetric DTMs[cite: 3]
* Georeferenced vector contour layers with custom labeling (`.gpkg` / `.shp`)[cite: 3]
* Comparative spatial analysis visualizations[cite: 3]

---<img width="847" height="552" alt="image_2026-09-14_203843158" src="https://github.com/user-attachments/assets/efbc574d-fd1f-42ee-83bf-e8e138c796d8" />
<img width="494" height="335" alt="image_2026-09-14_203930752" src="https://github.com/user-attachments/assets/eceb4810-38e9-4b58-8f68-9771b9e16f2c" />
<img width="864" height="601" alt="image_2026-09-14_203915036" src="https://github.com/user-attachments/assets/b44dcc85-0d11-485c-9f69-36a6c44ff150" />


## Author & Academic Context
* **Author:** Cofariu Diana-Elena ( alongside team members Manilici Andreea and Pinteala Georgiana - Group 7304)[cite: 3]
* **Academic Context:** Laboratory coursework developed for the **Photogrammetry 2 & GIS** curriculum at the Faculty of Hydrotechnics, Geodesy and Environmental Engineering, Technical University "Gheorghe Asachi" of Iași[cite: 3].
