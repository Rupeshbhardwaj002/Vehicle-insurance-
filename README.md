# 🚗 Vehicle Insurance Prediction – End-to-End MLOps Pipeline

An **industry-grade Machine Learning project** implementing a **complete MLOps pipeline** for predicting whether a customer will purchase vehicle insurance.

This project demonstrates **production-ready ML engineering practices** such as:

- End-to-End ML pipeline
- CI/CD automation
- Docker containerization
- AWS cloud integration
- Modular project architecture
- Logging & exception handling
- Artifact versioning and model storage

The goal is to simulate how **real-world ML systems are built, deployed, and maintained in production environments.**

---

# 📌 Problem Statement

Insurance companies often struggle to identify **which customers are likely to purchase vehicle insurance**.

Using machine learning, this system predicts **customer purchase intent**, enabling companies to:

- Target high-probability customers
- Optimize marketing campaigns
- Increase insurance conversion rates

---

# ⭐ Project Highlights

- ✔ End-to-End Machine Learning Pipeline  
- ✔ CI/CD Automation with **GitHub Actions**  
- ✔ Dockerized ML Application  
- ✔ **AWS S3** for model artifact storage  
- ✔ **AWS IAM** for secure authentication  
- ✔ **AWS ECR** for container registry  
- ✔ Modular and scalable architecture  
- ✔ Config-driven pipeline  

---

# 🏗 System Architecture


Data Source
│
▼
Data Ingestion
│
▼
Data Validation
│
▼
Data Transformation
│
▼
Model Training
│
▼
Model Evaluation
│
▼
Model Pusher
│
▼
AWS S3 Bucket
│
▼
Prediction Pipeline (Flask Web App)


---

# 📂 Project Structure

```bash
Vehicle-Insurance-Pipeline
│
├── .github/
│   └── workflows/
│       └── aws.yaml                # CI/CD workflow
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
├── artifact/                      # training artifacts
├── logs/                          # pipeline logs
├── notebook/                      # experimentation notebooks
├── templates/                     # HTML templates
├── static/                        # CSS files
│
├── Dockerfile
├── app.py
├── pyproject.toml
└── README.md
⚙️ ML Pipeline Stages
1️⃣ Data Ingestion

Fetch raw dataset

Store data in feature store

Split dataset into train and test sets

2️⃣ Data Validation

Schema validation

Missing value checks

Data consistency verification

3️⃣ Data Transformation

Feature engineering

Encoding categorical variables

Scaling numerical features

Save preprocessing pipeline

4️⃣ Model Training

Train machine learning model

Configure hyperparameters

Save trained model artifact

5️⃣ Model Evaluation

Evaluate model performance

Prevent poor models from deployment

6️⃣ Model Pusher

Push trained model artifacts to AWS S3

☁️ AWS Cloud Integration

This project integrates with AWS services to support production ML deployment.

AWS Service	Purpose
AWS S3	Model artifact storage
AWS IAM	Secure access control
AWS ECR	Docker container registry
GitHub Actions	CI/CD automation
🔁 CI/CD Pipeline

The CI/CD workflow automatically:

Builds Docker image

Pushes Docker image to AWS ECR

Deploys updated pipeline

Stores model artifacts in AWS S3

Workflow configuration:

.github/workflows/aws.yaml
🐳 Docker Containerization
Build Docker Image
docker build -t vehicle-insurance .
Run Docker Container
docker run -p 5000:5000 vehicle-insurance
🌐 Web Application

A Flask-based web application provides a simple interface for predictions.

Run locally:

python app.py

Open in browser:

http://localhost:5000
📊 Logging System

All pipeline logs are stored inside the logs directory.

logs/

Logs help monitor:

Pipeline execution

System errors

Debugging information

🛠 Tech Stack
Programming

Python

Machine Learning

Scikit-learn

Pandas

NumPy

MLOps Tools

Docker

GitHub Actions

AWS S3

AWS IAM

AWS ECR

Backend

Flask

🚀 Key Learning Outcomes

This project demonstrates practical knowledge of:

End-to-End Machine Learning Systems

MLOps engineering practices

CI/CD for ML pipelines

Cloud-based model deployment

Containerized ML applications

👨‍💻 Author

Rupesh Bhardwaj

AI / Machine Learning Engineer
Focused on Machine Learning, Deep Learning, and MLOps Systems
