pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/simba657/python-ci.git'
            }
        }
        stage('Install Dependencies') {
            steps {
                sh 'pip install -r requirements.txt'
            }
        }
        stage('Run Tests') {
            steps {
                sh 'pytest'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
                // Add deployment steps here, e.g., using AWS CLI to upload to S3 or deploy to EC2
                // sh 'aws s3 cp myapp.zip s3://mybucket/'
                // sh 'aws ec2 start-instances --instance-ids i-1234567890abcdef0'
            }
        }
    }
}

