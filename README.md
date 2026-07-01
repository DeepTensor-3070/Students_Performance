<div align="center">

# 📊 Student Performance Prediction System

### 🎓 An End-to-End Machine Learning Web Application that Predicts Student Mathematics Performance

[![Python](https://img.shields.io/badge/Python-3.12-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![FastAPI](https://img.shields.io/badge/FastAPI-Framework-009688?style=for-the-badge&logo=fastapi&logoColor=white)](https://fastapi.tiangolo.com/)
[![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![NumPy](https://img.shields.io/badge/NumPy-Array-013243?style=for-the-badge&logo=numpy&logoColor=white)](https://numpy.org/)
[![Render](https://img.shields.io/badge/Deployed%20on-Render-46E3B7?style=for-the-badge&logo=render&logoColor=white)](https://render.com/)
[![GitHub](https://img.shields.io/badge/GitHub-Repo-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/DeepTensor-3070/Students_Performance)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)](LICENSE)

</div>

---

## 📖 Introduction

The **Student Performance Prediction System** is a complete, production-ready **Machine Learning web application** that predicts a student's **Mathematics score** based on demographic, social, and academic indicators. Built with a fully modular ML pipeline and a FastAPI-powered web interface, this project demonstrates industry-standard practices for taking a machine learning model from raw data all the way to a deployed, user-facing application.

This project is designed to reflect **real-world ML engineering practices** — clean architecture, reusable pipelines, proper logging and exception handling, and a deployment-ready backend — making it a strong showcase for recruiters, collaborators, and fellow ML/MLOps enthusiasts.

---

## 🧭 Project Overview

| | |
|---|---|
| 🎯 **Goal** | Predict a student's Math score using ML |
| 🧠 **Approach** | Supervised Regression |
| 🏗️ **Architecture** | Modular, Pipeline-Based |
| 🌐 **Interface** | FastAPI + Jinja2 Web App |
| ☁️ **Deployment** | Render (Cloud Hosting) |

---

## ❓ Problem Statement

Educational institutions often lack data-driven tools to **proactively identify students who may need academic support**. Without predictive insight, interventions tend to be reactive rather than preventive, which can negatively impact student outcomes.

There is a need for a system that can:

- Analyze factors influencing student performance (gender, ethnicity, parental education, lunch type, test preparation, etc.)
- Predict a student's expected Math score based on these factors
- Present this prediction through an accessible, easy-to-use web interface

---

## 💡 Solution

This project solves the problem by building a **complete end-to-end ML pipeline**:

1. **Ingesting** raw student data
2. **Validating and Transforming** it using Scikit-learn pipelines
3. **Training and Evaluating** multiple regression models to select the best performer
4. **Serializing** the final model and preprocessor
5. **Serving predictions** through a FastAPI backend
6. **Presenting results** via a clean, responsive HTML frontend

The result is a deployable web application where a user can input student attributes and instantly receive a predicted Math score.

---

## ✨ Features

- ✅ End-to-End Machine Learning Pipeline
- 🧩 Modular, Industry-Standard Project Architecture
- 📥 Automated Data Ingestion
- 🔄 Data Transformation using Scikit-learn Pipelines
- 🛠️ Feature Engineering
- 🤖 Model Training across Multiple Algorithms
- 🏆 Automated Model Selection based on Evaluation Metrics
- 💾 Model Persistence via Pickle Serialization
- 🔮 Dedicated Prediction Pipeline
- ⚡ FastAPI-Powered Web Application
- 🎨 Responsive HTML/CSS Frontend with Jinja2 Templating
- 📝 Centralized Logging and Custom Exception Handling
- ☁️ Production Deployment on Render

---

## 🛠️ Tech Stack

### ⚙️ Backend

| Technology | Purpose |
|---|---|
| Python 3.12 | Core Programming Language |
| FastAPI | Web Framework / API Layer |
| Uvicorn | ASGI Server |
| Scikit-learn | Machine Learning Pipelines & Models |
| Pandas | Data Manipulation |
| NumPy | Numerical Computation |

### 🧠 Machine Learning

- Data Ingestion Pipeline
- Data Validation
- Data Transformation Pipeline
- Model Training
- Model Evaluation
- Prediction Pipeline
- Pickle Serialization

### 🎨 Frontend

| Technology | Purpose |
|---|---|
| HTML5 | Page Structure |
| CSS3 | Styling |
| Jinja2 Templates | Server-Side Rendering |

### ☁️ Deployment

- Render (Cloud Hosting)
- GitHub (Version Control & CI Source)

---

## 🔬 Machine Learning Pipeline

The ML workflow follows a clean, modular sequence:

```
Raw Data → Data Ingestion → Data Validation → Data Transformation
   → Model Training → Model Evaluation → Model Selection
   → Model Serialization (Pickle) → Prediction Pipeline
```

1. **Data Ingestion** — Reads raw data, splits it into training and test sets, and stores artifacts.
2. **Data Validation** — Ensures schema and data quality before transformation.
3. **Data Transformation** — Applies Scikit-learn `Pipeline` and `ColumnTransformer` for scaling, encoding, and imputation.
4. **Model Training** — Trains multiple regression algorithms (e.g., Linear Regression, Random Forest, Gradient Boosting, XGBoost, etc.).
5. **Model Evaluation** — Compares models using metrics such as R² Score to select the best-performing one.
6. **Model Saving** — Serializes the best model and preprocessing object as `.pkl` files in the `artifacts/` directory.
7. **Prediction Pipeline** — Loads the saved model and preprocessor to generate real-time predictions from new input data.

---

## 🏗️ Project Architecture

```
┌────────────────────┐
│   Raw Dataset       │
└─────────┬───────────┘
          ▼
┌────────────────────┐
│  Data Ingestion      │
└─────────┬───────────┘
          ▼
┌────────────────────┐
│ Data Transformation  │
└─────────┬───────────┘
          ▼
┌────────────────────┐
│   Model Trainer       │
└─────────┬───────────┘
          ▼
┌────────────────────┐
│  Artifacts (.pkl)    │
└─────────┬───────────┘
          ▼
┌────────────────────┐
│ Prediction Pipeline   │
└─────────┬───────────┘
          ▼
┌────────────────────┐
│  FastAPI Web App      │
└────────────────────┘
```

---

## 📁 Folder Structure

```text
project/
│
├── app.py
├── requirements.txt
├── setup.py
├── README.md
├── artifacts/
│   ├── model.pkl
│   └── preprocessor.pkl
│
├── templates/
│   ├── index.html
│   └── home.html
│
├── notebook/
│
├── src/
│   ├── components/
│   │   ├── data_ingestion.py
│   │   ├── data_transformation.py
│   │   └── model_trainer.py
│   │
│   ├── pipeline/
│   │   └── predict_pipeline.py
│   │
│   ├── exception.py
│   ├── logger.py
│   └── utils.py
│
├── logs/
│
└── artifacts/
```

---

## 🚀 Installation

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/DeepTensor-3070/Students_Performance.git
```

```bash
cd Students_Performance
```

### 2️⃣ Create Virtual Environment

```bash
python -m venv venv
```

**Activate the environment:**

Linux / macOS

```bash
source venv/bin/activate
```

Windows

```bash
venv\Scripts\activate
```

### 3️⃣ Install Requirements

```bash
pip install -r requirements.txt
```

---

## ▶️ Running the Project Locally

### Run with Uvicorn

```bash
uvicorn app:app --reload
```

The application will be available at:

```
http://127.0.0.1:8000
```

---

## 🔌 FastAPI Endpoints

| Method | Endpoint       | Description                   |
|--------|----------------|--------------------------------|
| GET    | `/`            | 🏠 Landing Page                |
| GET    | `/predictdata` | 📝 Prediction Form              |
| POST   | `/predictdata` | 🔮 Predict Student Math Score   |

---

## 📚 Interactive API Documentation

FastAPI automatically generates interactive API docs. Once the server is running, visit:

- **Swagger UI:** `http://127.0.0.1:8000/docs`
- **ReDoc:** `http://127.0.0.1:8000/redoc`

---

## ☁️ Deployment on Render

This project is configured for seamless deployment on **[Render](https://students-performance-deeptensor.onrender.com)**.

### Steps:

1. Push your code to GitHub.
2. Create a new **Web Service** on Render and connect your GitHub repository.
3. Configure the build and start commands as shown below.
4. Deploy 🚀

### 🔧 Render Build Command

```bash
pip install -r requirements.txt
```

### ▶️ Render Start Command

```bash
uvicorn app:app --host 0.0.0.0 --port $PORT
```

> ℹ️ **Note:** Render automatically provides the `$PORT` environment variable at runtime — no manual configuration is required for the port binding.

---

## 🔑 Environment Variables

This project does not require any mandatory environment variables to run locally. If you extend the project (e.g., add a database or third-party API), document them here in a `.env` file, for example:

```env
DATABASE_URL=your_database_url
SECRET_KEY=your_secret_key
```

---



## 🔮 Future Enhancements

- 🐳 Docker Support for Containerized Deployment
- 🔄 CI/CD Pipeline with GitHub Actions
- 📈 MLflow Integration for Experiment Tracking
- ☁️ AWS Deployment (EC2 / Elastic Beanstalk / S3)
- ☸️ Kubernetes Orchestration
- 🔐 User Authentication & Authorization
- 🗄️ Database Integration for Storing Predictions
- 📊 Real-Time Monitoring & Alerting
- 📋 Logging Dashboard for Observability
- 🏷️ Model Versioning & Registry

---

## 🎓 Learning Outcomes

Building this project involved hands-on experience with:

- Designing modular, production-grade ML project architecture
- Building reusable Scikit-learn transformation and prediction pipelines
- Implementing custom logging and exception-handling frameworks
- Serving ML models through a FastAPI backend
- Rendering dynamic frontends with Jinja2 templating
- Deploying a full-stack ML application to a live cloud platform (Render)

---

## 🤝 Contributing

Contributions are welcome and appreciated! To contribute:

1. **Fork** this repository
2. **Create** a new branch (`git checkout -b feature/your-feature-name`)
3. **Commit** your changes (`git commit -m "Add: your feature"`)
4. **Push** to your branch (`git push origin feature/your-feature-name`)
5. **Open** a Pull Request

Please make sure your code follows the existing project structure and style conventions.

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

## 👤 Author

**Subhanshu Verma (Deep Tensor)**
B.Tech CSE Student | ML/AI Enthusiast | Competitive Hackathon Builder

---

## 🔗 Connect with Me

[![GitHub](https://img.shields.io/badge/GitHub-DeepTensor--3070-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/DeepTensor-3070)

---

<div align="center">

### ⭐ If you found this project useful, consider giving it a star on GitHub!

</div>