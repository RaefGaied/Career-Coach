# AI Module - UtopiaHire

This module handles job matching using AI and NLP for the UtopiaHire platform.

## Project Structure

```
ai-module/
├── data/                   # Raw and processed data
├── preprocessing/         # Data cleaning and feature engineering
├── models/               # Trained models and vectorizers
├── api/                  # FastAPI application
└── utils/                # Configuration and utilities
```

## Setup

1. Install dependencies:
```bash
pip install -r requirements.txt
```

2. Configure environment variables in `.env`

3. Run the API:
```bash
uvicorn api.main:app --reload
```

ai-module/
├── data/
│   ├── raw_jobs.csv
│   ├── cleaned_jobs.csv
│   └── user_profiles.json
├── preprocessing/
│   ├── cleaner.py
│   └── feature_integration.py
├── models/
│   ├── job_match_model.pkl
│   ├── vectorizer.pkl
│   └── similarity.py (intègre résultats NLP)
├── api/
│   ├── main.py (FastAPI)
│   ├── routes/recommendations.py
│   └── routes/analysis.py
└── utils/
    ├── config.yaml
    └── evaluate.py

┌─────────────────────────────────────────────────────────────┐
│                  UTOPIAHIRE - SYSTÈME COMPLET                │
└─────────────────────────────────────────────────────────────┘

┌──────────────┐      ┌──────────────┐      ┌──────────────┐
│   FRONTEND   │ ───> │   BACKEND    │ ───> │   DATABASE   │
│  (React.js)  │ <─── │  (Node.js)   │ <─── │  (MongoDB)   │
└──────────────┘      └──────────────┘      └──────────────┘
                             │
                             ├─────> ┌──────────────┐
                             │       │  NLP SERVICE │
                             │       │  (Houusem)   │
                             │       └──────────────┘
                             │
                             └─────> ┌──────────────┐
                                     │  AI SERVICE  │
                                     │   (Flask)    │
                                     └──────────────┘

