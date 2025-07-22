# Flask CI/CD Template

This is a simple Flask application template used to demonstrate a basic CI/CD pipeline with Jenkins.

## Project Setup

1.  Clone the repository.
2.  Install dependencies: `pip install -r requirements.txt`
3.  Run the app: `python app.py`

## Jenkins Setup & Troubleshooting Notes

This project was used to set up a Jenkins pipeline. The following issues were encountered and resolved during setup:

* **Java Not Installed**: The initial Jenkins startup failed because Java was not installed on the system.
    * **Fix**: Installed Java using `sudo apt install openjdk-17-jre-headless`.

* **Incorrect Branch Name**: The pipeline failed to check out code because it was looking for the `master` branch by default.
    * **Fix**: Updated the **Branch Specifier** in the Jenkins job configuration to `*/main`.

* **Incorrect Jenkinsfile Path**: The pipeline failed with "Unable to find Jenkinsfile" after the file was moved.
    * **Fix**: Updated the **Script Path** in the Jenkins job configuration to `jenkins/Jenkinsfile`.
