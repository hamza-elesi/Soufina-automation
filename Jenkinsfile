pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'master', url: 'https://github.com/hamza-elesi/Soufina-automation.git'
            }
        }
        stage('Build') {
            steps {
                bat 'python -m pip install --upgrade pip' // Correct command to upgrade pip
                bat 'pip install -r requirements.txt'
            }
        }
        stage('Test') {
            steps {
                bat 'python -m unittest discover -s src'
            }
        }
        stage('Deploy') {
            steps {
                bat 'deploy.bat'
            }
        }
    }
}
