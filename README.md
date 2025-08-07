# 🌲 Forest Health Assessment in the Sierra Nevada Mountains (2018–2022)

This project evaluates changes in forest health over four years (2018 to 2022) using high-resolution **NAIP multispectral imagery** and **LiDAR data** in the **Sierra Nevada Mountains, California**. By leveraging remote sensing and object-based image analysis (OBIA), we quantify vegetation health trends before and after significant wildfire events using ArcGIS Pro and Trimble eCognition.

---

## 📍 Project Overview

Forest health monitoring using remote sensing enables efficient detection of stressed and diseased vegetation without the need for intensive field labor. In this project, we:
- Perform **image segmentation and classification** using OBIA methods.
- Analyze vegetation health using **NDVI** thresholds and LiDAR-derived **canopy height (nDSM)**.
- Calculate change in vegetation health over time using **area statistics** and **accuracy assessment**.

> Study Area: Lassen National Forest near **Lake Almanor**, CA (~0.6 mi²)

---

## ❓ Research Questions

1. How has forest health changed between 2018 and 2022?
2. What is the percent change in healthy, stressed, and diseased trees?
3. How reliable are the classifications using accuracy metrics?
4. Can NDVI and LiDAR-derived height data reliably detect post-fire vegetation stress?

---

## 🗂️ Data Sources

| Data Type | Source | Details |
|----------|--------|---------|
| **Multispectral Imagery** | USGS Earth Explorer (NAIP) | 0.6m resolution, 4-band (R, G, B, NIR) |
| **LiDAR Elevation Data** | USGS 3DEP Program | 0.5m resolution; used for DSM, DTM, and nDSM |
| **Study Boundary** | Manually clipped to overlapping imagery | Southern shore of Lake Almanor, CA |

---

## 🛠️ Tools & Software

- **ArcGIS Pro** – Image preprocessing, geospatial analysis, and mapping
- **Trimble eCognition** – Object-based image analysis, segmentation, and classification
- **Excel** – Accuracy assessment, error matrices, and tabular summaries
- **LASTools** – LiDAR format conversion (LAZ to LAS)

---

## 🔄 Methodology

1. **Data Preparation**
   - Download NAIP imagery and LiDAR data (2018 and 2022).
   - Convert LiDAR from `.laz` to `.las`, then derive DSM, DTM, and nDSM.

2. **Image Clipping & Projection**
   - Align all datasets to a common CRS (NAD 1983 UTM Zone 10N).
   - Clip imagery to study boundary.

3. **Object-Based Image Analysis (eCognition)**
   - Segment images using Quadtree and Multiresolution algorithms.
   - Create classification rules using NDVI thresholds and texture/height features:
     - Healthy Trees: NDVI > 0.6
     - Stressed Trees: NDVI 0.2–0.6
     - Diseased Trees: NDVI < 0.2

4. **Export & Post-Classification**
   - Export results as shapefiles for analysis in ArcGIS Pro.
   - Quantify area by class and calculate percent change (2018 vs. 2022).
   - Perform accuracy assessment using stratified random points and confusion matrices.

---

## 📊 Results Summary

| Class            | 2018 (acres) | 2022 (acres) | % Change |
|------------------|--------------|--------------|----------|
| Healthy Trees    | 93.49        | 0            | **-100%** |
| Stressed Trees   | 230.91       | 320.05       | **+38.6%** |
| Diseased Trees   | 9.72         | 13.23        | **+36.1%** |

**Key Findings:**
- Complete loss of healthy trees from 2018 to 2022.
- Significant increase in both stressed and diseased vegetation.
- Results likely impacted by the 2018 *Camp Fire*, California’s deadliest wildfire to date.

---

## ✅ Accuracy Assessment

| Metric           | 2018 (%) | 2022 (%) |
|------------------|----------|----------|
| Overall Accuracy | 75.6     | 70.7     |
| Producer's Accuracy (Trees) | ≥ 80%    | ≥ 80%    |
| User's Accuracy (Trees)     | ≥ 80%    | ≥ 80%    |

> Classification was most robust for tree health classes. Lower accuracy occurred for manmade features (buildings, pavement).

---

## 🗺️ Visuals

Add the following maps and figures in the `/figures/` directory:

- **Study Area Map**  
  ![A cartoon dinosaur wearing a party hat](https://i.imgur.com/fejzYEA.jpeg)

- **Classified Forest Health Maps**  
  ![2018 Classified Forest Health Map](https://i.imgur.com/iukhq4Z.jpeg)
need to add 2022 map

- **NDVI Range Table**  
  `figures/ndvi_thresholds.png`

- **Workflow Diagram**  
  `figures/processing_workflow.png`

---

## 📁 Repo Structure

