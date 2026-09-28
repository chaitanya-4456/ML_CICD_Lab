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
                bat '"C:\\Users\\chait\\ML_CICD_Lab\\venv\\Scripts\\python.exe" --version'
                bat '"C:\\Users\\chait\\ML_CICD_Lab\\venv\\Scripts\\pip.exe" install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                bat '"C:\\Users\\chait\\ML_CICD_Lab\\venv\\Scripts\\python.exe" -m pytest'
            }
        }

        stage('Build') {
            steps {
                echo 'Build completed successfully!'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment successful!'
            }
        }
    }
}