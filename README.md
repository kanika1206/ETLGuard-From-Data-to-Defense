## 🛡️ ETLGuard: From Data to Defense

ETLGuard is a production-grade, end-to-end MLOps pipeline for phishing website detection.
It automates the complete machine learning lifecycle — from data ingestion and validation to model training, experiment tracking, and real-time prediction — following industry-inspired MLOps and ETL design principles.

The project focuses on automation, reproducibility, modularity, and deployment readiness, making it suitable for real-world cybersecurity and ML engineering use cases.

## 🚀 Live Demo (Production Deployment)
🌐 Deployed on Render
 https://etlguard-from-data-to-defense.onrender.com

 ⚠️ Note: Render may take ~20–30 seconds to spin up on the first request.

 ## To Run Locally with Docker (Reproducibility)
 ```bash 
 docker build -t etlguard .
 docker run -p 8000:8000 etlguard
 ```
 ## Swagger UI (Local):
 ```bash
 http://localhost:8000/docs

 ```

 ## Introduction
 With the rapid growth of internet usage, phishing attacks have become one of the most prevalent cybersecurity threats. Phishing websites impersonate legitimate platforms to steal sensitive user information such as login credentials, banking details, and personal data. As these attacks evolve rapidly, automated and reliable detection mechanisms are critical for ensuring online safety.

ETLGuard addresses this challenge by implementing a structured, automated machine learning pipeline that transforms raw data into deployable phishing detection models using modern MLOps practices.

## Motivation Behind the Project
Traditional rule-based phishing detection systems struggle to adapt to evolving attack patterns. While machine learning-based approaches are more effective, many fail in production due to:

     1. Manual and error-prone ML experimentation
     2. Lack of automated data validation
     3. Absence of data drift detection
     4. Poor experiment tracking and        reproducibility
     5. Unstructured and non-scalable pipelines

ETLGuard solves these challenges by implementing a fully automated, modular ETL + ML pipeline, ensuring consistent execution across environments using Docker.


## Why Phishing Detection Matters

     1. A significant portion of cyberattacks originate from phishing attempts
     2. Users frequently interact with malicious links unknowingly
     3. Phishing causes large-scale financial and data losses annually
     4. Automated ML-based detection significantly reduces attack success rates
     5. Real-time detection helps prevent credential theft and data breaches

## Project Overview
ETLGuard is designed as a modular ML pipeline, inspired by real-world MLOps workflows used in production systems.

## High-Level Pipeline Flow

Raw Data -> Data Ingestion ->Data Validation (Schema + Drift Detection) -> Data Transformation -> Model Training -> Model Training -> Model Evaluation -> Prediction API

Each stage produces versioned artifacts to ensure traceability and reproducibility.

## Core Objectives
     1. Automate data ingestion, validation, transformation, and training
     2. Detect schema issues and data drift automatically
     3. Track experiments and model artifacts using MLflow
     4. Expose predictions via a REST API
     5. Ensure reproducibility using Docker-based execution

## Pipeline Components

#### 🔹 Data Ingestion

     1. Ingests structured phishing datasets
     2. Stores raw data in MongoDB
     3. Splits data into training and testing sets
     4. Generates timestamped ingestion artifacts

#### 🔹 Data Validation

     1. Validates schema consistency and column integrity
     2. Detects data drift between datasets
     3. Generates validation and drift reports

#### 🔹 Data Transformation

     1. Handles missing values using KNN-based imputation
     2. Applies feature preprocessing pipelines
     3. Saves transformed NumPy arrays and preprocessing objects

#### 🔹 Model Training & Evaluation

     1. Trains multiple classification models
     2. Selects the best model based on evaluation metrics
     3. Stores trained models and evaluation artifacts

#### 🔹 Deployment Readiness

     1. Stores finalized models as versioned artifacts
     2. Docker image can be deployed to cloud platforms

### Key Features

     1. Automated ETL + ML pipeline
     2. Schema validation and data drift detection
     3. Experiment tracking using MLflow
     4. Reproducible artifact management
     5. REST API for training and prediction
     6. Dockerized execution for consistency

### Tech Stack

Language: Python
Machine Learning: Scikit-learn, Pandas, NumPy
MLOps: MLflow
Backend: FastAPI, Uvicorn
Database: MongoDB
CI/CD: GitHub Actions
Containerization: Docker


## API Endpoints

<<<<<<< HEAD
## Technical Overview

### Backend Framework
- FastAPI with Uvicorn server

### Model Management
- MLflow for tracking experiments and model artifacts

### Containerization
- Docker ensures consistent runtime across systems

---

## How to Run the Project Locally (Docker)

```bash
docker build -t etlguard .
docker run -p 8000:8000 etlguard
```
---

## Swagger UI:
http://localhost:8000/docs


## Demo 

The application is deployed on Render.
Here's the link for the same : https://etlguard-from-data-to-defense.onrender.com

Available Endpoints

GET / – Health check

GET /train – Train the phishing detection model

POST /predict – Predict whether a URL is phishing or legitimate


## Cloud Readiness Note

The project is designed to be cloud-ready, but it currently runs locally using Docker. Cloud deployment components are optional and not required for running or demonstrating the project.
=======
| Method | Endpoint   | Description                        |
| ------ | ---------- | ---------------------------------- |
| GET    | `/`        | Health check                       |
| GET    | `/train`   | Trigger model training             |
| POST   | `/predict` | Predict phishing vs legitimate URL |
>>>>>>> 6ad6d95 (Update Readme)

## Cloud Readiness
ETLGuard is cloud-ready by design.
While currently deployed on Render, the system can be easily extended to other cloud platforms such as AWS, Azure, or GCP with minimal changes.

## Conclusion
<<<<<<< HEAD

ETLGuard demonstrates how modern MLOps practices can be applied to cybersecurity problems. By automating the complete ML lifecycle and exposing predictions through a structured API, the project provides a scalable and reproducible approach to phishing detection. Docker-based execution ensures consistency, while MLflow enables transparent experiment tracking, making the system suitable for further extension.
=======
ETLGuard demonstrates how modern MLOps and ETL principles can be applied to cybersecurity challenges. By automating the complete ML lifecycle from raw data ingestion to real time prediction the project provides a scalable, reproducible, and production ready approach to phishing detection.
>>>>>>> 6ad6d95 (Update Readme)
