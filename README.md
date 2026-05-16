# Aditya L1: Solar Flare Impact Analysis ☀️
### Space Weather Forecasting & Mitigation Research

> Predicting high-intensity solar flare impacts on Earth's communication and power infrastructure — using ISRO's Aditya L1 mission data.

[![Python](https://img.shields.io/badge/Python-Analysis-3776AB?logo=python)](https://python.org/)
[![XGBoost](https://img.shields.io/badge/XGBoost-ML_Model-FF6600)](https://xgboost.readthedocs.io/)
[![Research](https://img.shields.io/badge/Status-Paper_In_Review-brightgreen)]()
[![Program](https://img.shields.io/badge/Thapar-Satellite_Program-blue)]()

---

## Overview

This project is part of the **Thapar Satellite Program** and focuses on analysing data from ISRO's Aditya L1 mission — India's first dedicated solar observatory — to model and predict the severity of solar flare impacts on terrestrial systems.

Solar flares and Coronal Mass Ejections (CMEs) pose serious threats to satellite communications, GPS systems, and power grids. This work applies machine learning to real and simulated mission data to build a preliminary early-warning model, with a co-authored research paper currently under review.

---

## Research Scope

- 100+ hours of research across Aditya L1's 7 scientific payloads and mission objectives
- Analysis of 5,000–6,000 rows of real and simulated satellite data
- Coverage of 20+ CME events and solar wind pattern datasets
- Applied XGBoost classifier achieving **75.6% accuracy** in impact severity prediction
- Co-authored peer-reviewed paper on mitigation strategies for high-intensity solar flare events

---

## Aditya L1 Payloads Covered

| Payload | Purpose |
|---|---|
| VELC | Continuous solar corona imaging |
| SUIT | UV imaging of photosphere and chromosphere |
| SoLEXS | Soft X-ray spectrometer for flare monitoring |
| HEL1OS | Hard X-ray flare detection |
| ASPEX | Solar wind particle analysis |
| PAPA | Proton and alpha particle detection |
| MAG | In-situ magnetic field measurements at L1 |

---

## Machine Learning Model

**Model:** XGBoost Classifier  
**Target:** Solar flare impact severity (low / moderate / high)  
**Accuracy:** 75.6% (preliminary)

**Features used:**
- X-ray flux intensity (SoLEXS/HEL1OS)
- CME speed and angular width
- Solar wind velocity and density (ASPEX)
- Magnetic field B-component readings (MAG)
- Flare class (A/B/C/M/X)

**Pipeline:**
- Rolling window features (7-day mean, std, max)
- Rate of change via .diff()
- Exponentially Weighted Moving Averages (EWMA)
- Chronological train/test split (80/20)
- StandardScaler fitted only on training data
- Sliding window (3-day lag) for supervised learning format
- Sample weights to handle class imbalance (M and X class flares)

---

## Project Structure

    aditya-l1-solar-analysis/
    ├── data/
    │   └── Solar_Flare_dataset_final.csv
    ├── notebooks/
    │   └── Model2.ipynb
    ├── .gitignore
    └── README.md

---

## Getting Started

    git clone https://github.com/archiee04/aditya-l1-solar-analysis.git
    cd aditya-l1-solar-analysis
    pip install xgboost scikit-learn pandas numpy matplotlib seaborn jupyter
    jupyter notebook notebooks/Model2.ipynb

---

## Key Findings

- Solar flares classified as M and X class show the highest correlation with communication disruption events
- CME speed >1000 km/s is the strongest single predictor of high-severity impact
- Magnetic field fluctuations at L1 precede ground-level effects by approximately 15–60 minutes, offering a viable early-warning window

---

## Research Output

- 3 Technical Reports delivered to faculty and peers
- 2 Presentations combining analytical insights with science communication
- 1 Co-authored peer-reviewed paper (under review) on mitigation strategies for high-intensity solar flare impacts on communication and power systems

---

## References

- [ISRO Aditya L1 Mission](https://www.isro.gov.in/Aditya_L1.html)
- [NOAA Space Weather Prediction Center](https://www.swpc.noaa.gov/)
- [NASA Solar Dynamics Observatory](https://sdo.gsfc.nasa.gov/)

---

## Author

**Archie Srivastava** — [LinkedIn](https://linkedin.com/in/archie-srivastava-36b81835b) · [Email](mailto:archie.srivastava04@gmail.com)  
Thapar Institute of Engineering & Technology, Patiala
