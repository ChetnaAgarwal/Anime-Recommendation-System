# Anime-Recommendation-System
MLOps Project using GCP, Kubernetes, Docker, DVC


Scalable, containerized, and production-ready Anime Recommendation System using **content-based**, **collaborative filtering**, and **hybrid** models. Designed to increase retention, engagement, and revenue for anime streaming platforms like **Crunchyroll**.

---

## 🚀 Overview

This project builds a recommendation engine leveraging user-anime interaction data to serve personalized recommendations in real time. It employs a modular MLOps pipeline and scales efficiently using **GCP Kubernetes Engine (GKE)**.

---

## 🎯 Use Case

Target audience: Anime streaming platforms (e.g., Crunchyroll)

**Goals**:
- Enhance viewer **retention rate**
- Expand user **base and engagement**
- Increase **platform revenue**

---

## 🧠 Recommender System Types

| Type                  | Description |
|-----------------------|-------------|
| **Content-Based**     | Recommends anime similar in genre/tags to what a user has liked |
| **Collaborative Filtering** | Recommends based on preferences of similar users |
| **Hybrid Approach**   | Combines both strategies for improved personalization |

---

## 📦 Dataset

- Source: [Anime Recommendation Database 2020](https://www.kaggle.com/datasets)
- Size: ~2 GB
- Contains: 3.2M users, 16K animes, 70M interaction rows
- Sample used: **5M rows**

---

## 🛠️ Tech Stack

- **Data Engineering**: GCP Buckets, DVC
- **Modeling**: Scikit-learn, Pandas, Surprise
- **Experiment Tracking**: CometML
- **Pipeline & Versioning**: DVC + GitHub
- **Deployment**: Docker, GCR, Jenkins, Kubernetes (GKE)

---

## ⚙️ Workflow

### 🔧 Project Setup & Ingestion
- Data upload to GCP Buckets
- Manual upload for demo
- Selective ingestion: Sampled 5M rows from the full dataset

### 📊 Data Processing & Modeling
- Conducted inside Jupyter Notebooks initially, later modularized using Python classes
- Implemented:
  - Feature engineering
  - Content similarity computation
  - User-item matrix generation
  - Hybrid scoring function

### 🧪 Training & Experimentation
- Tracked hyperparameters, metrics, and model versions via **CometML**
- Combined experiment tracking with training pipeline for seamless iteration

### 🔄 Version Control
- Code: GitHub
- Data: DVC linked with a dedicated GCP Bucket

### 🔍 Prediction Helpers
- Built prediction APIs from notebook logic
- Integrated into app logic to fetch and serve live recommendations

### 🚢 CI/CD & Deployment
- Containerized with Docker and pushed to **Google Cloud Registry (GCR)**
- Deployed via **Kubernetes on GKE**
- **Jenkins pipeline** automates build → test → deploy stages

