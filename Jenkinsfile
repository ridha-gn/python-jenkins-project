pipeline {
    agent {
        docker {
            image 'python:3.11'  // or 3.10, 3.9, etc.
        }
    }

    environment {
        PYTHONUNBUFFERED = 1
    }

    stages {
        stage('Install Dependencies') {
            steps {
                sh 'pip install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'pytest test_main.py'
            }
        }
    }
}


