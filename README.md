# End-to-End MLOps Project

This repository contains an end-to-end Machine Learning Operations (MLOps) pipeline for **house price prediction**, demonstrating a production-ready workflow—from data ingestion and preprocessing, to model training, evaluation, API deployment (Flask & FastAPI), and containerization using Docker.

---

## 🚀 Project Structure

```

.
├── api/
│   └── fastapi\_app.py
├── data/
│   └── house\_prices.csv
├── flask\_app/
│   ├── app.py
│   ├── static/
│   └── templates/
├── models/
│   ├── house\_price\_model.pkl
│   └── scaler.pkl
├── Pipeline/
│   ├── data\_pipeline.py
│   └── data\_train.py
├── requirements.txt
├── Dockerfile
├── docker-compose.yml
└── README.md

````

---

## 🛠️ Key Features

- **Automated Data Pipeline:** End-to-end workflow for data cleaning, preprocessing, and feature engineering.
- **Model Training:** Trains a Random Forest Regressor for house price prediction.
- **Model Serialization:** Saves trained models and scalers as `.pkl` files for reproducible deployment.
- **API Integration:**
  - **Flask:** Simple web app for interactive predictions.
  - **FastAPI:** High-performance REST API for programmatic access.
- **Containerization:** Docker support for easy, reproducible deployments across environments.

---

## ⚙️ Setup & Usage

### 1. Clone the Repository

```bash
git clone https://github.com/dhanush-github/End-to-End-MLOps-Project.git
cd End-to-End-MLOps-Project
````

### 2. Create Virtual Environment & Install Dependencies

```bash
# Using conda (recommended)
conda create -n mlops_env python=3.11
conda activate mlops_env
pip install -r requirements.txt
```

### 3. Run the Data Pipeline and Train Model

```bash
cd Pipeline
python data_train.py
```

### 4. Run the Flask App

```bash
cd ../flask_app
python app.py
```

Visit [http://localhost:5000](http://localhost:5000) in your browser.

### 5. Run the FastAPI App

```bash
cd ../api
uvicorn fastapi_app:app --reload
```

API docs available at [http://localhost:8000/docs](http://localhost:8000/docs)

### 6. Docker Deployment (Optional)

```bash
docker build -t mlops-project .
docker run -p 5000:5000 mlops-project
```

---

## 🧩 Files & Directories Explained

* **api/**: FastAPI application for model inference.
* **flask\_app/**: Flask web app for simple UI-based predictions.
* **data/**: Datasets for training/testing.
* **models/**: Serialized trained model and preprocessing objects.
* **Pipeline/**: Scripts for data processing and model training.
* **requirements.txt**: Python dependencies.
* **Dockerfile**: Containerization config.
* **docker-compose.yml**: (Optional) Multi-container orchestration.

---

## 💡 Project Highlights

* End-to-end implementation of an MLOps workflow.
* Reproducible environment via requirements.txt and Docker.
* Both web UI and API endpoints for flexible serving.
* Easily extensible for other ML tasks or deployment pipelines.

---


---

**To use:**  
1. Create a new file named `README.md` at your project root.
2. Paste the above content.
3. Save and push:

```sh
git add README.md
git commit -m "Add complete project README"
git push
````


