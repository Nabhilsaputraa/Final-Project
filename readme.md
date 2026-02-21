# Injury Risk Prediction

## Overview
Proyek ini menggunakan **Machine Learning (Random Forest)** untuk memprediksi risiko cedera atlet dalam jangka pendek. Sistem ini memperhitungkan **faktor latihan, pemulihan, stres, dan biomekanik** untuk memberikan rekomendasi berbasis data dan jurnal ilmiah.  
Model dilengkapi dengan **Streamlit Dashboard** untuk visualisasi risiko dan insight yang mudah dipahami.

## Features
- Prediksi risiko cedera: **Low / Medium / High**  
- Estimasi probabilitas cedera  
- Identifikasi faktor risiko utama: Training Load, Sleep, Stress, Muscle Asymmetry, Flexibility  
- Rekomendasi berbasis data dan penelitian ilmiah  
- API FastAPI untuk integrasi ke aplikasi lain  

## Project Structure
├── app/
│ ├── inference.py # Fungsi prediksi risiko cedera
│ ├── schema.py # Input data model Pydantic
│ └── main.py # FastAPI endpoints
├── src/
│ ├── data/
│ │ └── preprocessing.py # Preprocessing & feature engineering
│ └── models/
│ ├── logistic_regression.py
│ └── random_forest.py
├── artifacts/ # Model & preprocessor hasil training
├── frontend/ # Streamlit dashboard / frontend code
├── notebook/ # Exploratory notebooks
├── main.py # Script training utama
├── docker-compose.yml
├── Dockerfile
├── requirements.txt
└── README.md

## Installation

1. Clone repository:
```bash
git clone https://github.com/username/injury-risk-prediction.git
cd injury-risk-prediction

2. Buat virtual environment dan install dependencies:
python -m venv venv
source venv/bin/activate 
venv\Scripts\activate     
pip install -r requirements.txt

Usage
1. Run API
uvicorn app.main:app --reload
2. Run Dashboard
streamlit run app.py
- Masukkan data atlet di dashboard
- Klik Analyze Injury Risk untuk melihat prediksi & rekomendasi

Results
- Prediksi risiko cedera: Low / Medium / High
- Confidence (probabilitas)
- Visualisasi faktor risiko utama
- Rekomendasi berbasis penelitian ilmiah

Conclusion & Recommendation
AI model berfungsi sebagai early warning system untuk risiko cedera atlet
Faktor paling berpengaruh: tidur, pemulihan, stress, ketidakseimbangan otot, fleksibilitas