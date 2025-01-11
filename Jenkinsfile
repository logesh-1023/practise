pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out code from repository'
                git 'https://github.com/logesh-1023/practise.git'
            }
        }
        stage('Build') {
            steps {
                echo 'Building the project'
                sh 'echo "Building the project..."'
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests'
                sh 'echo "Running tests..."'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying to environment'
                sh 'echo "Deploying to environment..."'
            }
        }
    }
}
