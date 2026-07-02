# AgriSense – Automated Geospatial Intelligence for Precision Agriculture

A geospatial data science project that processes Sentinel-2 satellite imagery to monitor crop conditions using spectral analysis, image preprocessing, unsupervised learning, and change detection. The project explores how remote sensing and machine learning can be combined to support precision agriculture.

---

# Overview

Precision agriculture increasingly relies on satellite imagery to monitor crop health over large areas. However, raw satellite data is often affected by atmospheric conditions, cloud cover, and the lack of labeled datasets for supervised learning.

AgriSense explores a complete geospatial workflow that transforms multispectral Sentinel-2 imagery into actionable agricultural insights using image preprocessing, vegetation indices, clustering, and temporal change detection.

The project focuses on building a reproducible pipeline rather than a single machine learning model.

---

# Features

* Satellite image preprocessing
* Atmospheric correction workflow
* Vegetation index generation
* Multispectral feature engineering
* Unsupervised land-cover clustering
* Crop stress monitoring
* Temporal change detection
* GIS-ready outputs

---

### Programming

* Python
* NumPy
* Pandas
* SciPy
* Scikit-learn

### Geospatial

* Google Earth Engine
* Geemap
* Rasterio
* GeoPandas
* Py6S

### Deep Learning

* PyTorch

### Visualization

* Matplotlib
* OpenCV

---

#  Processing Pipeline

```text
Sentinel-2 Imagery
        │
        ▼
Atmospheric Correction
        │
        ▼
Image Enhancement
        │
        ▼
Spectral Index Generation
        │
        ▼
Feature Stack
        │
        ▼
Land Cover Clustering
        │
        ▼
Temporal Change Detection
        │
        ▼
Maps & GIS Outputs
```

---

#  Project Components

## 1. Atmospheric Preprocessing

Satellite imagery is first corrected to reduce atmospheric effects before further analysis.

The workflow includes:

* Top-of-Atmosphere (TOA) to Bottom-of-Atmosphere (BOA) reflectance correction
* Dark Object Subtraction (DOS-1)
* Image normalization

These preprocessing steps improve consistency across images acquired on different dates.

---

## 2. Image Enhancement

Satellite imagery can be degraded by haze and cloud cover.

The project investigates deep learning approaches such as:

* AOD-Net for haze removal
* Partial Convolutions (PConv) for cloud inpainting

These techniques help improve image usability before downstream analysis.

---

## 3. Spectral Feature Engineering

Instead of relying only on RGB imagery, the project extracts multiple vegetation indices from multispectral bands.

Indices include:

| Index | Purpose                  |
| ----- | ------------------------ |
| NDVI  | Vegetation health        |
| EVI   | Biomass estimation       |
| SAVI  | Soil-adjusted vegetation |
| MSAVI | Early crop monitoring    |
| NDWI  | Water stress detection   |
| NDRE  | Chlorophyll estimation   |
| LAI   | Leaf density estimation  |

Combining these indices provides a richer representation of crop conditions than individual bands alone.

---

## 4. Land Cover Classification

Because labeled agricultural datasets are often unavailable, the project applies unsupervised clustering.

K-Means clustering is used on the multispectral feature stack to identify major land-cover groups, including:

* Healthy vegetation
* Sparse vegetation
* Bare soil
* Water bodies
* Other land-cover types

---

## 5. Change Detection

Temporal imagery is compared using Change Vector Analysis (CVA).

The objective is to identify significant spectral changes between two observation dates that may indicate:

* crop stress
* irrigation issues
* harvesting
* seasonal vegetation changes

---


# 📊 Outputs

Depending on the workflow, the project can generate:

* Vegetation index maps
* Clustered land-cover maps
* Crop stress maps
* Geo-referenced CSV files
* ESRI Shapefiles
* Visualization plots

---


# What I Learned

This project strengthened my understanding of:

* Remote sensing fundamentals
* Geospatial data processing
* Multispectral image analysis
* Feature engineering using vegetation indices
* Unsupervised machine learning
* GIS data formats
* Deep learning for image restoration
* End-to-end data science workflows


# Future Improvements

Possible extensions include:

* Semantic segmentation using U-Net
* Time-series forecasting for crop growth
* Transformer-based remote sensing models
* Automated cloud masking
* Interactive web dashboard
* Integration with weather and soil datasets



