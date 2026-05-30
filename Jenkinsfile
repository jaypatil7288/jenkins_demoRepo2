pipeline {
    agent any
    
    // Poll SCM trigger: polls every 2 minutes
    triggers {
        pollSCM('H/2 * * * *')
    }
    
    stages {
        stage('Checkout') {
            steps {
                // This step automatically checks out code from the SCM configured in the job
                checkout scm
                echo 'Source code checked out successfully.'
            }
        }
        stage('Build') {
            steps {
                echo 'Building the application...'
                // E.g., sh 'npm install' or sh 'make' goes here
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                // E.g., sh 'npm test' goes here
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying application to server...'
                // E.g., deployment scripts go here
            }
        }
    }
}
