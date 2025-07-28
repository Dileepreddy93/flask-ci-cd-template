# Flask CI/CD Project with Jenkins and Render

[![Build Status](http://YOUR_JENKINS_URL/job/Flask-ci-cd-template/badge/icon)](http://YOUR_JENKINS_URL/job/YOUR_PRO/Flask-ci-cd-template)

This repository contains a sample Flask web application configured with a complete CI/CD pipeline. The pipeline uses Jenkins for continuous integration (testing) and automatically deploys the application to Render upon a successful build.

## ✨ Features

- **Backend:** A lightweight web server using the Flask framework.
- **Frontend:** A simple user interface built with standard HTML, CSS, and JavaScript.
- **CI/CD Pipeline:** An automated pipeline managed by a `Jenkinsfile`.
- **Automated Testing:** Unit tests are run automatically with `pytest` on every push.
- **Automated Deployment:** The application is deployed to Render automatically after all tests pass.

## 🛠️ Tech Stack

- **Backend:** Python 3, Flask
- **Frontend:** HTML, CSS, JavaScript
- **CI/CD:** Jenkins, Git
- **Hosting:** Render
- **Testing:** pytest

## 🚀 Local Setup

To run this project on your local machine, follow these steps.

**Prerequisites:**
- Python 3.8+
- `pip` and `venv`
- Git

**Installation:**
1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/dileepreddy93/YOUR_REPOSITORY.git](https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git)
    cd YOUR_REPOSITORY
    ```
2.  **Create and activate a virtual environment:**
    ```bash
    # For macOS/Linux
    python3 -m venv venv
    source venv/bin/activate
    ```
3.  **Install the dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
4.  **Run the application:**
    ```bash
    python app.py
    ```
5.  Open your browser and navigate to `http://127.0.0.1:5000`.

## 🔄 CI/CD Pipeline Overview

The CI/CD pipeline is designed to ensure code quality and automate deployments.

1.  **Trigger:** A `git push` to the `main` branch automatically triggers the Jenkins pipeline.
2.  **Install Dependencies:** Jenkins creates a clean environment and installs all required packages from `requirements.txt`.
3.  **Test:** The `pytest` test suite is executed. If any test fails, the pipeline stops.
4.  **Deploy to Render:** If all tests pass, Jenkins sends a request to a secure **Deploy Hook**, which tells Render to pull the latest code and deploy the new version of the application.

## 🌐 Deployment

This application is hosted on Render and is updated automatically by the CI/CD pipeline.

The live application is available at: **[https://YOUR_APP_NAME.onrender.com](https://YOUR_APP_NAME.