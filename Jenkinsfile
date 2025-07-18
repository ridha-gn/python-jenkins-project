pipeline {
    agent {
        docker {
            image 'python:3.10'
        }
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
                sh 'pytest test_main.py'
            }
        }
    }
}

