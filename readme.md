# Injury Risk Prediction

Proyek ini menggunakan Machine Learning (Random Forest) untuk memprediksi risiko cedera atlet dalam jangka pendek. Sistem ini mempertimbangkan faktor latihan, pemulihan, stres, dan biomekanik.
Model dilengkapi dengan Streamlit Dashboard untuk visualisasi risiko dan insight yang mudah dipahami.

## Features
- Prediksi risiko cedera: Low / Medium / High
- Estimasi probabilitas cedera
- Identifikasi faktor risiko utama: Training Load, Sleep, Stress, Muscle Asymmetry, Flexibility
- Rekomendasi berbasis data dan penelitian ilmiah
- API FastAPI untuk integrasi ke aplikasi lain

## Project Structure
```bash
├── app/
│   ├── inference.py        
│   ├── schema.py            
│   └── main.py              
├── src/
│   ├── data/
│   │   └── preprocessing.py 
│   └── models/
│       ├── logistic_regression.py
│       └── random_forest.py
├── artifacts/               
├── frontend/                
├── notebook/                
├── main.py                  
├── Dockerfile
├── docker-compose.yml
├── requirements.txt
└── README.md
```

## Installation

1. Clone repository: 

```bash
git clone https://github.com/username/injury-risk-prediction.git
cd injury-risk-prediction
```

2. Buat virtual environment dan install dependencies:

```bash
python -m venv venv        
source venv/bin/activate   # Linux / macOS
venv\Scripts\activate      # Windows
pip install -r requirements.txt
```

## Usage
1. Run API
```python
uvicorn app.main:app --reload
```
2. Run Dashboard
```python
streamlit run frontend/app.py
```
- Masukkan data atlet di dashboard
- Klik Analyze Injury Risk untuk melihat prediksi & rekomendasi

## Results
- Prediksi risiko cedera: Low / Medium / High
- Confidence (probabilitas)
- Visualisasi faktor risiko utama

## Conclusion & Recommendation
Model AI berfungsi sebagai early warning system untuk risiko cedera atlet.
Faktor paling berpengaruh: tidur, pemulihan, stres, ketidakseimbangan otot, fleksibilitas.
