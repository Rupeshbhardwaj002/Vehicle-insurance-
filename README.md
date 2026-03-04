🚗 Vehicle Insurance Prediction – End-to-End MLOps Pipeline

An industry-grade Machine Learning project implementing a complete MLOps pipeline for predicting whether a customer will purchase vehicle insurance.

This project demonstrates production-ready ML engineering practices, including:

End-to-End ML pipeline

CI/CD automation

Docker containerization

AWS cloud integration

Modular and scalable architecture

Logging and exception handling

Artifact management

The goal is to simulate how real-world ML systems are built and deployed in production environments.

📌 Problem Statement

Insurance companies often struggle to identify which customers are likely to purchase vehicle insurance.

Using machine learning, this system predicts customer purchase intent, allowing companies to:

Optimize marketing campaigns

Target potential customers

Increase insurance conversion rates

🧠 Key Features

✔ End-to-End ML Pipeline
✔ Modular Project Architecture
✔ CI/CD using GitHub Actions
✔ AWS S3 for artifact storage
✔ AWS IAM for secure cloud access
✔ AWS ECR for Docker image registry
✔ Dockerized ML service
✔ Config-driven pipeline
✔ Logging and exception handling

🏗 System Architecture
                ┌───────────────────────┐
                │      Data Source      │
                └──────────┬────────────┘
                           │
                           ▼
                ┌───────────────────────┐
                │    Data Ingestion     │
                └──────────┬────────────┘
                           │
                           ▼
                ┌───────────────────────┐
                │    Data Validation    │
                └──────────┬────────────┘
                           │
                           ▼
                ┌───────────────────────┐
                │ Data Transformation   │
                └──────────┬────────────┘
                           │
                           ▼
                ┌───────────────────────┐
                │    Model Training     │
                └──────────┬────────────┘
                           │
                           ▼
                ┌───────────────────────┐
                │   Model Evaluation    │
                └──────────┬────────────┘
                           │
                           ▼
                ┌───────────────────────┐
                │     Model Pusher      │
                └──────────┬────────────┘
                           │
                           ▼
                ┌───────────────────────┐
                │      AWS S3 Bucket    │
                └──────────┬────────────┘
                           │
                           ▼
                ┌───────────────────────┐
                │  Prediction Pipeline  │
                │      (Flask App)      │
                └───────────────────────┘
📂 Project Structure
Vehicle-Insurance-Pipeline
│
├── .github/workflows/
│   └── aws.yaml                # CI/CD pipeline
│
├── src/
│   ├── components/
│   │   ├── data_ingestion.py
│   │   ├── data_validation.py
│   │   ├── data_transformation.py
│   │   ├── model_trainer.py
│   │   ├── model_evaluation.py
│   │   └── model_pusher.py
│   │
│   ├── pipeline/
│   │   ├── training_pipeline.py
│   │   └── prediction_pipeline.py
│   │
│   ├── cloud_storage/
│   │   └── aws_storage.py
│   │
│   ├── configuration/
│   │   ├── aws_connection.py
│   │   └── mongo_db_connection.py
│   │
│   ├── entity/
│   │   ├── config_entity.py
│   │   └── artifact_entity.py
│   │
│   └── utils/
│       └── main_utils.py
│
├── config/
│   ├── model.yaml
│   └── schema.yaml
│
├── artifact/                   # training artifacts
├── logs/                       # pipeline logs
├── notebook/                   # experimentation notebooks
├── templates/                  # html templates
├── static/                     # css files
│
├── app.py
├── Dockerfile
├── pyproject.toml
└── README.md
⚙️ ML Pipeline Stages
1️⃣ Data Ingestion

Fetch dataset

Store raw data

Split data into train/test sets

2️⃣ Data Validation

Validate schema

Check missing values

Data consistency checks

3️⃣ Data Transformation

Feature engineering

Encoding categorical variables

Scaling numerical features

Save preprocessing pipeline

4️⃣ Model Training

Train ML model

Configure hyperparameters

Save trained model

5️⃣ Model Evaluation

Compare model performance

Ensure quality threshold before deployment

6️⃣ Model Pusher

Upload model artifacts to AWS S3

☁️ AWS Cloud Integration

The project integrates with AWS services to support production deployment.

Service	Purpose
AWS S3	Model artifact storage
AWS IAM	Secure authentication
AWS ECR	Docker image registry
GitHub Actions	CI/CD automation
🔁 CI/CD Pipeline

The CI/CD workflow automatically:

Builds Docker image

Pushes image to AWS ECR

Deploys updated pipeline

Stores artifacts in AWS S3

Workflow file location:

.github/workflows/aws.yaml
🐳 Docker Containerization

Build Docker Image

docker build -t vehicle-insurance .

Run Container

docker run -p 5000:5000 vehicle-insurance
🌐 Web Application

A Flask-based web interface is used for real-time predictions.

Run locally:

python app.py

Access in browser:

http://localhost:5000
📊 Logging System

Pipeline logs are stored in:

logs/

This helps monitor:

pipeline execution

errors

debugging

🛠 Tech Stack
Programming

Python

Machine Learning

Scikit-learn

Pandas

NumPy

MLOps

Docker

GitHub Actions

AWS S3

AWS IAM

AWS ECR

Backend

Flask

🚀 Learning Outcomes

This project demonstrates practical knowledge of:

Production Machine Learning systems

End-to-End ML pipelines

MLOps engineering

Cloud integration

CI/CD automation

Containerized ML deployment

👨‍💻 Author

Rupesh Bhardwaj

AI / Machine Learning Engineer
Interested in Deep Learning, MLOps, and Scalable AI Systems