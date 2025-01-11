pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/yourusername/your-repo.git'
            }
        }
        stage('Install Dependencies') {
            steps {
                script {
                    sh 'pip install -r requirements.txt'
                }
            }
        }
        stage('Train Model') {
            steps {
                script {
                    sh 'python train_model.py'
                }
            }
        }
        stage('Test Model') {
            steps {
                script {
                    sh 'python test_model.py'
                }
            }
        }
        stage('Deploy to AWS') {
            steps {
                script {
                    sh 'aws s3 cp model.pkl s3://your-bucket-name/model.pkl'
                }
            }
        }
    }
    post {
        success {
            echo 'Pipeline successfully executed!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
