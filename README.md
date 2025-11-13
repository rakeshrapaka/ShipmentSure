Goal: Build a reproducible pipeline that predicts shipment risk (delay / damage / loss / customs hold) and returns a probability + color-coded risk signal (Green / Orange / Red) with a small demo UI for users to input shipment details and receive a risk score.


shipmentsure/
├─ data/
│  ├─ raw/                # original datasets (shipment logs, carriers, weather, etc.)
│  └─ processed/          # cleaned & merged datasets
├─ notebooks/
│  ├─ 01_EDA.ipynb
│  ├─ 02_preprocessing.ipynb
│  └─ 03_models_eval.ipynb
├─ src/
│  ├─ ingest.py           # data ingestion + joins (carrier, route, weather)
│  ├─ preprocess.py
│  ├─ features.py
│  ├─ train.py
│  ├─ evaluate.py
│  └─ serve_api.py        # FastAPI inference service
├─ serve/
│  └─ app_streamlit.py    # demo UI (input form + risk signal)
├─ models/
│  └─ best_model.joblib
├─ requirements.txt
├─ README.md
└─ LICENSE
