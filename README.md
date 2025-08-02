<div align="center">

# 🚀 Flask CI/CD Template
### *Professional DevOps Pipeline with Jenkins & Render*

[![Build Status](https://img.shields.io/badge/Build-Passing-brightgreen?style=for-the-badge&logo=jenkins)](http://YOUR_JENKINS_URL/job/Flask-ci-cd-template/)
[![Deploy Status](https://img.shields.io/badge/Deploy-Live-success?style=for-the-badge&logo=render)](https://flask-ci-cd-template.onrender.com)
[![Python](https://img.shields.io/badge/Python-3.8+-blue?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![Flask](https://img.shields.io/badge/Flask-3.1.1-red?style=for-the-badge&logo=flask&logoColor=white)](https://flask.palletsprojects.com/)
[![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)](LICENSE)

*A complete CI/CD pipeline template featuring automated testing, security scanning, and seamless deployment to production*

</div>

---

## 🌟 **Overview**

This repository showcases a **production-ready Flask web application** with a fully automated CI/CD pipeline. Experience the power of modern DevOps practices with automated testing, security scanning, and zero-downtime deployments.

<div align="center">

### 🎯 **Live Demo**
**[🌐 View Live Application](https://flask-ci-cd-template.onrender.com)**

</div>

---

## ✨ **Key Features**

<table>
<tr>
<td width="50%">

### 🔧 **Backend Excellence**
- 🐍 **Python 3.8+** with Flask framework
- 🔒 **Security-first** approach
- 📦 **Containerized** with Docker
- 🚀 **Production-ready** configuration

</td>
<td width="50%">

### 🎨 **Frontend Elegance**
- 📱 **Responsive** design
- 🎨 **Modern** CSS styling
- ⚡ **JavaScript** interactivity
- 🌙 **Dark theme** interface

</td>
</tr>
<tr>
<td width="50%">

### 🔄 **DevOps Pipeline**
- 🤖 **Automated** CI/CD with Jenkins
- 🧪 **Unit testing** with pytest
- 🛡️ **Security scanning** with Trivy
- 📊 **Code quality** with Flake8

</td>
<td width="50%">

### ☁️ **Cloud Deployment**
- 🌐 **Render** hosting platform
- 🔗 **Webhook** integration
- 📈 **Auto-scaling** capabilities
- 🔧 **Zero-downtime** deployments

</td>
</tr>
</table>

---

## 🛠️ **Technology Stack**

<div align="center">

| Category | Technologies |
|----------|-------------|
| **Backend** | ![Python](https://img.shields.io/badge/Python-FFD43B?style=flat&logo=python&logoColor=blue) ![Flask](https://img.shields.io/badge/Flask-000000?style=flat&logo=flask&logoColor=white) |
| **Frontend** | ![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white) ![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white) ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black) |
| **DevOps** | ![Jenkins](https://img.shields.io/badge/Jenkins-D24939?style=flat&logo=jenkins&logoColor=white) ![Docker](https://img.shields.io/badge/Docker-2CA5E0?style=flat&logo=docker&logoColor=white) ![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white) |
| **Testing** | ![Pytest](https://img.shields.io/badge/Pytest-0A9EDC?style=flat&logo=pytest&logoColor=white) ![Flake8](https://img.shields.io/badge/Flake8-3776AB?style=flat&logo=python&logoColor=white) |
| **Security** | ![Trivy](https://img.shields.io/badge/Trivy-1904DA?style=flat&logo=aqua&logoColor=white) ![pip-audit](https://img.shields.io/badge/pip--audit-FF6B6B?style=flat&logo=pypi&logoColor=white) |
| **Hosting** | ![Render](https://img.shields.io/badge/Render-46E3B7?style=flat&logo=render&logoColor=white) |

</div>

---

## 🚀 **Quick Start Guide**

### 📋 **Prerequisites**

Before you begin, ensure you have:

- 🐍 **Python 3.8+** installed
- 📦 **pip** and **venv** available
- 🔧 **Git** for version control

### ⚡ **Installation**

<details>
<summary><b>🔽 Click to expand installation steps</b></summary>

1. **📥 Clone the Repository**
   ```bash
   git clone https://github.com/dileepreddy93/flask-ci-cd-template.git
   cd flask-ci-cd-template
   ```

2. **🔧 Setup Virtual Environment**
   ```bash
   # Create virtual environment
   python3 -m venv venv
   
   # Activate (Linux/macOS)
   source venv/bin/activate
   
   # Activate (Windows)
   venv\Scripts\activate
   ```

3. **📦 Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **🚀 Launch Application**
   ```bash
   python app.py
   ```

5. **🌐 Access Application**
   
   Open your browser and navigate to: **[http://127.0.0.1:5000](http://127.0.0.1:5000)**

</details>

---

## 🔄 **CI/CD Pipeline Architecture**

<div align="center">

```mermaid
graph TD
    A[👨‍💻 Developer Push] --> B[🔄 GitHub Webhook]
    B --> C[🏗️ Jenkins Trigger]
    C --> D[📦 Install Dependencies]
    D --> E[🛡️ Security Scan]
    E --> F[🧪 Run Tests]
    F --> G[🐳 Build Docker Image]
    G --> H[🔍 Image Security Scan]
    H --> I[🚀 Deploy to Render]
    I --> J[✅ Live Application]
    
    style A fill:#e1f5fe
    style C fill:#f3e5f5
    style F fill:#e8f5e8
    style I fill:#fff3e0
    style J fill:#e0f2f1
```

</div>

### 🔍 **Pipeline Stages**

| Stage | Description | Tools |
|-------|-------------|-------|
| **🔄 Trigger** | Automatic pipeline execution on `main` branch push | GitHub Webhooks |
| **📦 Dependencies** | Clean environment setup with all required packages | pip, venv |
| **🛡️ Security Scan** | Vulnerability assessment of dependencies | pip-audit |
| **🧪 Testing** | Comprehensive unit test execution | pytest |
| **🐳 Build** | Docker image creation and optimization | Docker |
| **🔍 Image Scan** | Container security vulnerability check | Trivy |
| **🚀 Deployment** | Automated deployment to production | Render Deploy Hook |

---

## 🌐 **Deployment Information**

<div align="center">

### 🚀 **Live Application**

**[🌟 Experience the Live Demo](https://flask-ci-cd-template.onrender.com)**

*Automatically updated through our CI/CD pipeline*

[![Deployment Status](https://img.shields.io/website?down_color=red&down_message=offline&style=for-the-badge&up_color=green&up_message=online&url=https%3A//flask-ci-cd-template.onrender.com)](https://flask-ci-cd-template.onrender.com)

</div>

---

## 🤝 **Contributing**

We welcome contributions! Please see our [Contributing Guidelines](CONTRIBUTING.md) for details.

<div align="center">

### 📫 **Get in Touch**

[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/dileepreddy93)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/dileepreddy93)

</div>

---

<div align="center">

### ⭐ **Star this repository if you found it helpful!**

[![Stars](https://img.shields.io/github/stars/dileepreddy93/flask-ci-cd-template?style=social)](https://github.com/dileepreddy93/flask-ci-cd-template/stargazers)
[![Forks](https://img.shields.io/github/forks/dileepreddy93/flask-ci-cd-template?style=social)](https://github.com/dileepreddy93/flask-ci-cd-template/network)

*Made with ❤️ for the DevOps community*

</div>