pipeline {
    agent any
    
    environment {
        DIRECTORY_PATH = "E:/SIT753/Week-5"
        TESTING_ENVIRONMENT = "testing"
        PRODUCTION_ENVIRONMENT = "new_production"
    }
    
    stages {
        stage('Build') {
            steps {
                echo "Fetching the source code from ${env.DIRECTORY_PATH} environment variable"
                echo "Compiling the code and generating any necessary artifacts"
            }
        }
        stage('Test') {
            steps {
                echo "Running unit tests"
                echo "Running integration tests"
            }
        }
        stage('Code Quality Check') {
            steps {
                echo "Checking the quality of the code"
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploying the application to ${env.TESTING_ENVIRONMENT} environment"
            }
        }
        stage('Approval') {
            steps {
                echo "Waiting for manual approval..."
                script {
                    sleep(time: 10, unit: 'SECONDS')
                }
            }
        }
        stage('Deploy to Production') {
            steps {
                echo "Deploying the code to the production environment ${env.PRODUCTION_ENVIRONMENT}"
            }
        }
    }
}
