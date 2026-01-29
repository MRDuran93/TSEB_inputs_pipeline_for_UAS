# TSEB Inputs Pipeline from UAS Multispectral Imagery (ArcGIS Pro)

**Moises Duran\*, Alfonso Torres**  
Utah State University – Agricultural Monitoring and Remote Sensing Lab  

---

## Overview

This repository contains **ArcGIS Pro–based Jupyter notebooks** to process **UAS multispectral imagery (MicaSense Altum-PT)** and generate **spatially resampled input variables for the Two-Source Energy Balance (TSEB) model** in **almond orchards**.

The workflow converts raw multispectral, thermal, and surface model data into gridded TSEB inputs suitable for high-resolution evapotranspiration studies.

---

## Pipeline Status (Ongoing Development)

This pipeline is **actively under development**. Current efforts focus on **consolidating the multiple notebooks into a single, streamlined workflow** and **migrating the processing to a fully Python-based, open-source implementation** (outside the ArcGIS Pro environment).  
This repository will be **updated regularly** as these improvements are completed.

---

## Generated TSEB Inputs

- Canopy Fractional Cover (FC)  
- Leaf Area Index (LAI)  
- Canopy Width  
- Canopy Height*  
- Width / Height ratio*  
- Canopy Thermal Temperature (corrected & resampled)

\*Height-related products are **experimental** and provided for testing only.

---

## Data & Environment

- **Sensor:** MicaSense Altum-PT  
- **Bands:** Blue, Green, Red, Red Edge, NIR, Thermal  
- **Grid resolution:** Default 6.5 m (user-defined)  
- **Platform:** ArcGIS Pro (arcpy + Spatial Analyst)

---

## Notebooks

- **Pipeline_part1** – NDVI-based canopy extraction, FC, Width, LAI, W/H  
- **Pipeline_part2** – Experimental height estimation from DSM → DTM (NDVI-masked, kriging)  
- **Pipeline_part2-2** – Alternative height estimation using external soil/terrain points  
- **Temperature_correction** – Thermal calibration and grid resampling (Altum-PT / AggieAir)

All notebooks require manual editing of **paths, band order, and grid size**.

---

## Notes & Limitations

- NDVI thresholds are calibrated for **almond orchards**  
- Height products are sensitive to **high canopy cover and field heterogeneity**  
- Thermal correction equations must be adapted to your calibration data

---

## Use & Citation Policy

If these notebooks contribute to a **scientific publication**, users agree to:
- Acknowledge the authors  
- Invite them to participate as **co-authors**

---

## Acknowledgements

This work was funded by the **Almond Board of California**, the **California Department of Food and Agriculture (CDFA) Specialty Crops Block Grant Program**, and **USDA-CRIS base funds**.  
We thank the **McElrone Lab** for sensor array deployment and physiological data collection, and the **AggieAir Service Center** for sUAS data collection and processing of flights conducted in **2021, 2022, 2023, and 2024**.

---

## Contact

**Moises Duran** – m.duran-gomez@usu.edu  
**Alfonso Torres** – alfonso.torres@usu.edu  


[README_inputs_TSEB.pdf](https://github.com/user-attachments/files/19237933/README_inputs_TSEB.pdf)
