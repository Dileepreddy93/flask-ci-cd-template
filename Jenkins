pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out source code...'
                // This step is usually handled by Jenkins automatically.
            }
        }
        stage('Install Dependencies') {
            steps {
                echo 'Installing Python packages...'
                // This command reads your requirements.txt file and installs the libraries.
                sh 'pip install -r requirements.txt'
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                // This is a common command to run tests using the pytest framework.
                // If you use a different testing tool, change this line.
                sh 'pytest'
            }
        }
    }
    post {
        // The 'post' section runs after all the stages are complete.
        always {
            echo 'Pipeline finished.'
        }
        success {
            echo 'Hooray! The pipeline was successful. ✅'
        }
        failure {
            echo 'Oops! The pipeline failed.'
        }
    }
}
