# Flask Web App with Security-Focused CI/CD Pipeline

![CI/CD Status](https://img.shields.io/badge/CI/CD-Passing-brightgreen?style=for-the-badge&logo=jenkins)

This project is a sample Flask web application demonstrating a modern, robust, and security-focused Continuous Integration and Continuous Deployment (CI/CD) pipeline using Jenkins. The entire pipeline is defined as code in the `Jenkinsfile`.

## ✨ Pipeline Features

This automated pipeline ensures that every code change is automatically built, tested, and scanned before deployment:

* **🤖 Automated Triggers**: The pipeline is automatically triggered by a `git push` to the GitHub repository via webhooks.
* **📦 Dockerized Environment**: All pipeline stages run inside clean, isolated Docker containers for consistency and predictability.
* **✅ Code Quality & Linting**: Automatically checks Python code style and quality using `Flake8`.
* **🧪 Unit Testing**: Runs unit tests using `Pytest` and publishes the results to the Jenkins dashboard.
* **🔒 Dependency Scanning**: Uses `pip-audit` to scan Python packages for known vulnerabilities.
* **🛡️ Container Image Scanning**: Uses `Trivy` to scan the final Docker image for OS-level vulnerabilities before pushing.
* **🚀 Automated Docker Builds**: Builds a production-ready, multi-stage Docker image of the application.
* **☁️ Conditional Deployment**: Automatically deploys the application only when changes are pushed to the `main` branch and all previous stages have passed.

## 🛠️ Technology Stack

* **Backend**: Flask, Gunicorn
* **Language**: Python 3.9
* **CI/CD**: Jenkins (Declarative Pipeline)
* **Containerization**: Docker
* **Testing & Analysis**: Pytest, Flake8, pip-audit, Trivy

## ⚙️ How the Pipeline Works

The `Jenkinsfile` orchestrates the entire process through a series of stages:

1.  **Install & Scan Dependencies**: Installs Python packages from `requirements.txt` and scans them for security vulnerabilities.
2.  **Lint & Test**: Enforces code style and runs all unit tests to ensure application correctness.
3.  **Build Docker Image**: Compiles the Flask application into a lightweight, optimized Docker image using a multi-stage `Dockerfile`.
4.  **Scan Docker Image for Vulnerabilities**: Performs a security scan on the newly built image. The pipeline will fail if any `HIGH` or `CRITICAL` severity vulnerabilities are found.
5.  **Push and Deploy**: If the pipeline is running on the `main` branch and all previous stages succeed, it pushes the verified Docker image to a container registry and executes the deployment script.

## 🚀 Getting Started

To set up this project and pipeline yourself:

1.  **Prerequisites**:
    * Jenkins instance with Docker installed and configured.
    * GitHub account.
    * Docker Hub account (or another container registry).

2.  **Clone the Repository**:
    ```sh
    git clone [https://github.com/your-username/your-repo.git](https://github.com/your-username/your-repo.git)
    cd your-repo
    ```

3.  **Configure Jenkins**:
    * **Add Credentials**: Go to `Manage Jenkins` > `Credentials` and add your Docker Hub credentials with a memorable ID (e.g., `dockerhub-credentials`).
    * **Create Pipeline Job**: Create a new "Pipeline" job in Jenkins.
    * **Point to Repository**: In the job configuration, under the "Pipeline" section, select "Pipeline script from SCM".
        * **SCM**: Git
        * **Repository URL**: Your repository's URL.
        * **Script Path**: `Jenkinsfile` (this is the default).

4.  **Set up GitHub Webhook**:
    * In your GitHub repository settings, go to `Webhooks` > `Add webhook`.
    * **Payload URL**: Enter your Jenkins URL followed by `/github-webhook/`. (You may need a tool like `ngrok` if your Jenkins is running locally).
    * **Content type**: `application/json`.

Now, every `git push` to your repository will automatically trigger your new, secure pipeline!

## 🐳 The Multi-Stage Dockerfile

This project uses a multi-stage `Dockerfile` to create a highly optimized and secure final image.

* **Builder Stage**: This stage installs all dependencies and prepares the application.
* **Final Stage**: This stage copies only the necessary application code and installed packages from the builder into a clean, slim base image. It also runs the application as a non-root user for enhanced security.

This strategy results in a smaller attack surface and a significantly reduced image size, making it faster to pull and cheaper to store.

---

*This README was last updated on July 23, 2025.*
