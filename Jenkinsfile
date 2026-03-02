pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git 'https://github.com/your-username/cicd-python-api.git'
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

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t cicd-python-api .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 5000:5000 cicd-python-api'
            }
        }
    }
}
