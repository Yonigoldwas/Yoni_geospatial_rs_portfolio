# Geospatial and remote sensing portfolio

I am a remote sensing agronomist with a masters degree in plant science.  
I work with satellite imagery, Google Earth Engine, Python, Jupyter, and Streamlit to build practical tools for agriculture, risk mapping and more.

This portfolio collects working projects and code examples that I share with companies and collaborators.

## Project categories

1. Crop monitoring and harvesting analysis in Google Earth Engine  
2. Crop classification and satellite embeddings  
3. Flood and risk mapping with radar data  
4. Computer vision on aerial imagery  
5. Decision support and market insight apps in Streamlit  

Each project below links to its own repository with code, usage instructions, and screenshots.

---

## 1. Crop monitoring and harvesting analysis in GEE

### 1.1 Harvest detection from NDVI for corn and soy

**Repository**  
`https://github.com/Yonigoldwas/gee_harvest_detection_ndvi.git`  

**Problem**  
Objectively detect harvest timing for corn and soy fields in a given region and period.

**Approach**  
1. Use Sentinel two surface reflectance imagery in Google Earth Engine  
2. Compute NDVI time series per field polygon  
3. Smooth the signal and detect the main drop that corresponds to harvest  
4. Export maps and tables with estimated harvest date per field

**Result**  
Maps and statistics that show when each field was harvested, ready to use for agronomy teams and insurance analysis.

---

### 1.2 Unsupervised crop classification with satellite embeddings

**Repository**  
`https://github.com/Yonigoldwas/gee_unsupervised_crop_classification_embeddings.git`

**Problem**  
Differentiate corn and soy fields over the corn belt using satellite embeddings, without relying only on classic vegetation indices.

**Approach**  
1. Use the Google satellite embedding dataset in GEE  
2. Combine with CDL information for corn and soy  
3. Apply clustering or simple classifiers in the embedding space  
4. Evaluate with confusion matrix and accuracy by region

**Result**  
Crop type maps and evaluation metrics that show how well simple methods can separate crops in the learned embedding space.

---

### 1.3 SAR flood mapping with change detection

**Repository**  
`gee_sar_flood_mapping_change_detection`

**Problem**  
Map flooded areas after an event and quantify the impact on agriculture and urban zones.

**Approach**  
1. Use Sentinel one radar imagery in GEE  
2. Build pre event and post event composites  
3. Apply a change detection rule on backscatter values  
4. Intersect flooded pixels with land cover data  
5. Calculate affected agricultural and urban areas

**Result**  
Flood extent maps and area statistics that support emergency response, reporting, and risk analysis.

---

### 1.4 Indices app for polygons

**Repository**  
`gee_indices_app_for_polygon`

**Problem**  
Give agronomists a simple way to explore indices for any field or polygon over time.

**Approach**  
1. GEE app where the user draws or uploads a polygon  
2. User selects date range  
3. App displays Sentinel two based indices NDVI, EVI and others as maps and time series  
4. Optionally export charts or data

**Result**  
Interactive tool that supports field scouting and remote crop assessment directly in the browser.

---

## 2. Crop classification with embeddings and adaptation

### 2.1 Embeddings based crop classification with adaptor

**Repository**  
`gee_embeddings_crop_classification_adaptor`

**Problem**  
Classify crop types corn, soybeans, wheat in a new season using a model trained on satellite embeddings from a previous year.

**Approach**  
1. Train a Random Forest on 2023 annual satellite embeddings with CDL labels  
2. Train a linear regression adaptor that maps July Sentinel two features to the embedding space  
3. Apply the adaptor to July 2024 Sentinel two imagery  
4. Classify 2024 pixels with the trained Random Forest  
5. Evaluate predictions against CDL 2024

**Result**  
A practical workflow that shows how to combine representation learning and simple models to generalize crop classification across years.

### 2.2 Corn and soy classification with GEE Python API

**Repository**  
`gee_python_corn_soy_classification`

**Summary**  
Supervised classification of corn and soy using Sentinel two data and the GEE Python API, implemented in a Colab style notebook with clear training, prediction, and evaluation steps.

---

## 3. Flood and risk mapping

Covered above in the SAR flood mapping project.  

Additional risk and event mapping projects will be added here in the future.

---

## 4. Computer vision on aerial imagery

### 4.1 Airplane detection in NAIP imagery with SAM three

**Repository**  
`cv_sam3_naip_airplane_detection`

**Problem**  
Detect airplanes in high resolution NAIP aerial imagery.

**Approach**  
1. Download NAIP tiles that cover a chosen bounding box  
2. Apply SAM three based image segmentation or classification to find airplanes  
3. Visualize detections on the imagery  
4. Optionally compute simple metrics precision and recall on a small labeled set

**Result**  
Example of applying modern vision models to remote sensing imagery in a Jupyter notebook environment.

---

## 5. Streamlit decision support and BI apps

### 5.1 NexusBI live market intelligence

**Repository**  
`streamlit_nexusbi_live_market_intel`

**Problem**  
Provide an interactive dashboard for share and market monitoring.

**Approach**  
1. Use Python to pull market data for selected symbols  
2. Compute indicators and aggregates  
3. Build a Streamlit app with time series charts, filters, and summary tables  
4. Deploy so that users can access it in a browser

**Result**  
A live BI style interface for exploring share performance and basic analytics.

---

### 5.2 Eto water balance and GDD tracker

**Repository**  
`streamlit_eto_water_balance_gdd_tracker`

**Problem**  
Help agronomists and growers track reference evapotranspiration water balance and growing degree days for a given area and period.

**Approach**  
1. Input location, time period, and basic crop or parameter settings  
2. Compute reference evapotranspiration and water balance over time  
3. Compute growing degree days  
4. Display charts and tables in a Streamlit app  
5. Allow export of the data if needed

**Result**  
A simple decision support tool that connects agrometeorological concepts with a clear user interface.

---

## Contact

If you are interested in any of these projects or want to see specific parts of the code, feel free to reach out.

You can also ask for custom examples or short case studies that match your use case.
