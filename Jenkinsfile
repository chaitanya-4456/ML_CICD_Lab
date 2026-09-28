pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Install Dependencies') {
            steps {
                bat 'py --version'
                bat 'py -m pip install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                bat 'py -m pytest -q'
            }
        }

        stage('Build') {
            steps {
                bat 'py app.py'
            }
        }

        stage('Deploy') {
            steps {
                bat 'echo Deployment Successful!'
            }
        }
    }
}