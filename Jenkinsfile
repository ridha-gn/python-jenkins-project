pipeline {
    agent any

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
                sh 'python3 -m pip install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'python3 -m pytest test_main.py'
            }
        }
    }
}

