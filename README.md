# ETLGuard: From Data to Defense

## Introduction

With the rapid growth of internet usage, phishing attacks have become one of the most prevalent cybersecurity threats. Phishing websites mimic legitimate platforms to steal sensitive user information such as passwords, banking credentials, and personal data. Detecting such malicious websites in a reliable and automated manner is critical for ensuring online safety.

ETLGuard is an end-to-end machine learning–based phishing detection system that automates the entire ML lifecycle—from data ingestion and validation to model training and prediction—using modern MLOps practices. The project emphasizes reproducibility, automation, and structured pipeline design.

---

## Motivation Behind the Project

Phishing attacks are continuously evolving, making traditional rule-based detection systems ineffective. Many machine learning solutions fail in practice due to the lack of proper data validation, experiment tracking, and reproducibility.

Key challenges addressed by this project:
- Manual ML experimentation is time-consuming and error-prone
- Lack of automated data validation leads to unreliable models
- Reproducing ML results across environments is difficult
- Security-focused ML pipelines often lack structured automation

ETLGuard solves these issues by implementing a fully automated and modular MLOps pipeline that can be executed consistently using Docker.

---

## Statistics Highlighting the Need for Phishing Detection

- Over 90% of cyberattacks begin with phishing attempts  
- 1 in 3 users has unknowingly interacted with a phishing link  
- Phishing attacks cause billions of dollars in losses annually  
- Automated ML-based detection systems can reduce phishing success rates by up to 70%  
- Real-time phishing detection significantly lowers credential theft and data breaches  

---

## Project Overview

ETLGuard is designed as a modular machine learning pipeline that automates all major stages of ML development for phishing detection.

### Core Objectives
- Automate data ingestion, validation, transformation, and training
- Track experiments and model performance using MLflow
- Provide prediction functionality through a REST API
- Ensure reproducibility using Docker-based execution

---

## Core Technologies Used

- Python  
- Scikit-learn, Pandas, NumPy  
- MLflow  
- FastAPI  
- Docker  
- GitHub Actions  
- MongoDB  

---

## Key Features

### Automated ETL Pipeline
- Ingests phishing datasets
- Validates data schema and detects inconsistencies
- Transforms features for model training

### Experiment Tracking
- Logs parameters, metrics, and artifacts using MLflow
- Ensures reproducibility of experiments

### Model Training and Evaluation
- Trains classification models for phishing detection
- Evaluates models using standardized performance metrics

### REST API Interface
- `/train` endpoint triggers model training
- `/predict` endpoint returns phishing predictions
- Interactive API testing via Swagger UI

### Dockerized Execution
- Entire application runs inside a Docker container
- Eliminates dependency and environment mismatch issues

---

## System Architecture

Raw Data
↓
Data Ingestion
↓
Data Validation
↓
Data Transformation
↓
Model Training
↓
Model Evaluation
↓
Prediction API


---

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


## Conclusion

ETLGuard demonstrates how modern MLOps practices can be applied to cybersecurity problems. By automating the complete ML lifecycle and exposing predictions through a structured API, the project provides a scalable and reproducible approach to phishing detection. Docker-based execution ensures consistency, while MLflow enables transparent experiment tracking, making the system suitable for further extension.
