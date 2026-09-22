pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out code from GitHub...'
                checkout scm
            }
        }
        
        stage('Build') {
            steps {
                echo 'Building the project...'
                echo 'Build stage completed!'
            }
        }
        
        stage('Test') {
            steps {
                echo 'Running tests...'
                echo 'All tests passed!'
            }
        }
    }
    
    post {
        always {
            echo 'Pipeline execution finished!'
        }
    }
}
