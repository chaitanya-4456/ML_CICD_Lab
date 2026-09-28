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
                bat '"C:\\Users\\chait\\AppData\\Local\\Programs\\Python\\Launcher\\py.exe" --version'
                bat '"C:\\Users\\chait\\AppData\\Local\\Programs\\Python\\Launcher\\py.exe" -m pip install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                bat '"C:\\Users\\chait\\AppData\\Local\\Programs\\Python\\Launcher\\py.exe" -m pytest -q'
            }
        }

        stage('Build') {
            steps {
                bat '"C:\\Users\\chait\\AppData\\Local\\Programs\\Python\\Launcher\\py.exe" app.py'
            }
        }

        stage('Deploy') {
            steps {
                bat 'echo Deployment Successful!'
            }
        }
    }
}