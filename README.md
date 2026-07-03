# Student Exam Performance Indicator

An end-to-end Machine Learning web application deployed on **AWS (Elastic Beanstalk + CodePipeline)** that predicts a student's math exam score based on demographic and academic background factors. 

This project demonstrates a complete MLOps lifecycle: from modular exploratory data analysis (EDA) and pipeline ingestion to automated cloud deployment and reverse proxy configurations.

---

## 🚀 Live Demo
🔗 **Production URL:** http://studentperformancesite-env-1.eba-viq8k3cu.eu-north-1.elasticbeanstalk.com/predictdata

---

## 📱 Application Preview

| Production UI | 
| <img width="1891" height="908" alt="Screenshot 2026-07-03 235800" src="https://github.com/user-attachments/assets/77da14d4-3654-4823-8fae-cfbf0023ad17" />




| CI/CD Automation |
 | <img width="1235" height="607" alt="Screenshot 2026-07-03 235649" src="https://github.com/user-attachments/assets/3a11d826-e0f4-41ec-9512-c3ee152cb24f" />



 | Environment Health |
 | <img width="1520" height="276" alt="Screenshot 2026-07-03 235706" src="https://github.com/user-attachments/assets/e4e4f601-bc47-415d-a0b8-433f35a5658c" />
 |

---

## 🏗️ System Architecture & CI/CD Flow

The system is engineered for continuous deployment. Any code update pushed to the repository automatically runs through a managed cloud release pipeline:


---

## 🛠️ Tech Stack & Engineering Highlights

* **Core ML & Data Pipeline:** Python, Scikit-Learn, Pandas, NumPy, Seaborn, Matplotlib.
* **Web Framework & Production Server:** Flask, Gunicorn.
* **Cloud Infrastructure (AWS):**
  * **Elastic Beanstalk:** Managed orchestration for hosting the runtime web app containers.
  * **CodePipeline:** Automated CI/CD pipeline integrated directly via GitHub App connections.
  * **IAM (Identity & Access Management):** Custom granular JSON policies enabling resource deployment clearance.
  * **EC2 & EBS Storage Management:** Scaled compute root volumes to accommodate dense mathematical serialization models.
  * **Nginx Reverse Proxy:** Customized upstream routing mechanisms connecting port `5000` execution targets cleanly.

---

## 📁 Repository Structure

```text
├── .elasticbeanstalk/     # AWS Elastic Beanstalk configuration scripts
├── artifacts/             # Serialized model (.pkl) and preprocessor objects
├── src/                   # Core application source code
│   ├── components/        # Data Ingestion, Data Transformation, Model Trainer
│   ├── pipeline/          # Training and Prediction execution pipelines
│   ├── exception.py       # Custom exception handling mechanism
│   └── logger.py          # Detailed system logging utilities
├── templates/             # HTML user interface assets (index.html, home.html)
├── application.py         # Main Flask web application entry point
├── Procfile               # Production WSGI server instruction file for AWS
├── requirements.txt       # Strict environment dependencies configuration
└── README.md              # Project documentation
