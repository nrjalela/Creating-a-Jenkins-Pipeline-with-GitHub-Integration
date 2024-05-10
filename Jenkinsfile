pipeline {
    agent any
    environment {
        DIRECTORY_PATH = "/dev"
        TESTING_ENVIRONMENT = "Task6.1C"
        PRODUCTION_ENVIRONMENT = "NiharJ"
    }
    stages {
        stage('Build') {
            steps {
                echo "Downloading the source code from $DIRECTORY_PATH"
                echo "Compiling the source code and creating artifacts"
            }
        }
        stage('Test') {
            steps {
                echo "Executing unit tests"
                echo "Performing integration tests"
            }
        }
        stage('Code Quality Check') {
            steps {
                echo "Analyzing the code quality"
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploying the application to $TESTING_ENVIRONMENT environment"
            }
        }
        stage('Approval') {
            steps {
                echo "Waiting for manual approval..."
                sleep 10
            }
        }
        stage('Deploy to Production') {
            steps {
                echo "Deploying the code to $PRODUCTION_ENVIRONMENT environment"
            }
        }
    }
}
