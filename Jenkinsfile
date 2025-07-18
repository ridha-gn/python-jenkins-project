pipeline {
    agent {
        docker {
            image 'python:3.11'
        }
    }

    environment {
        PYTHONUNBUFFERED = 1
    }

    stages {
        stage('Clone') {
            steps {
                git branch: 'main', url: 'https://github.com/ridha-gn/python-jenkins-project.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'pip install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'pytest tests/test_main.py'
            }
        }
    }
}

