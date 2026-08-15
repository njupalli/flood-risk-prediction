# 🌊 Flood Risk Prediction API & Geospatial ML Platform

A end-to-end machine learning system and REST API designed to predict localized flood risk from environmental geospatial datasets. Built with Scikit-Learn, deployed on AWS EC2 via FastAPI, and integrated into an interactive Tableau dashboard for real-time spatial analysis.

---

## 📊 Project Overview & Impact
* **Dataset Scale:** Trained and evaluated on over **4.6M+ geospatial data points** incorporating elevation, land slope, historical rainfall, and soil/land-use characteristics.
* **Model Pipeline:** Random Forest classification model achieving high accuracy on multi-layer spatial feature maps.
* **Real-time Pipeline:** Automated raster extraction engine using **Rasterio** and **NumPy** to execute coordinate transformations and handle missing or out-of-bound spatial data.
* **Cloud Infrastructure:** High-throughput REST API hosted on an **AWS EC2** instance configured for live geospatial inference queries.

---

## 🛠️ Tech Stack
* **Language:** Python 3.10
* **Machine Learning:** Scikit-Learn, NumPy, Pandas
* **Geospatial Processing:** Rasterio, GeoPandas, GDAL
* **API & Deployment:** FastAPI, Uvicorn, AWS EC2
* **Data Visualization:** Tableau

---

## 🏗️ Architecture & Data Flow

```text
[ Raw Geospatial Rasters ] ──> [ Feature Pipeline (Rasterio/NumPy) ] ──> [ Random Forest Model ]
                                                                                   │
[ Lat/Long Query ] ──────────> [ FastAPI REST Service (AWS EC2) ] <────────────────┘
                                              │
                                              ▼
                               [ Tableau Spatial Dashboard ]
