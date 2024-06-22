pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'master', url: 'https://github.com/hamza-elesi/automation-pipe.git'
            }
        }
        stage('Build') {
            steps {
                sh 'pip install -r requirements.txt'
            }
        }
        stage('Test') {
            steps {
                sh 'python -m unittest discover -s src'
            }
        }
        stage('Deploy') {
            steps {
                sh 'bash deploy.sh'
            }
        }
    }
}
