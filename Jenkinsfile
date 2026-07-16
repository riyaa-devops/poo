pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps { git 'YOUR_GITHUB_REPO_URL' }
        }
        stage('Build Docker Image') {
            steps { sh 'docker build -t flask-app .' }
        }
        stage('Run Docker Container') {
            steps { sh 'docker run -d -p 5000:5000 flask-app' }
        }
    }
}
