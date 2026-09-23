pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out code...'
                checkout scm
            }
        }
        
        stage('Build') {
            steps {
                echo 'Building project...'
                sh 'echo "Build stage completed"'
            }
        }
        
        stage('Parallel Tests') {
            parallel {
                stage('Unit Tests') {
                    steps {
                        echo 'Running unit tests...'
                        sh 'echo "Unit tests passed"'
                    }
                }
                stage('Integration Tests') {
                    steps {
                        echo 'Running integration tests...'
                        sh 'echo "Integration tests passed"'
                    }
                }
                stage('Code Quality') {
                    steps {
                        echo 'Checking code quality...'
                        sh 'echo "Code quality checks passed"'
                    }
                }
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                sh 'echo "Deployment successful"'
            }
        }
    }
    
    post {
        always {
            echo 'Pipeline execution completed!'
        }
        success {
            echo 'Build succeeded! ✅'
        }
        failure {
            echo 'Build failed! ❌'
        }
    }
}
