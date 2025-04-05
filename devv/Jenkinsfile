pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from the repository
                checkout scm
            }
        }

        stage('Build Docker Image') {
            steps {
                // Build the Docker image
                script {
                    sh 'docker build -t flask-app .'
                }
            }
        }

        stage('Run Docker Container') {
            steps {
                // Run the Docker container
                script {
                    sh 'docker run -d -p 5000:5000 --name flask-app-container flask-app'
                }
            }
        }
    }

    post {
        always {
            // Clean up Docker container after the pipeline finishes
            script {
                sh 'docker stop flask-app-container || true'
                sh 'docker rm flask-app-container || true'
            }
        }
    }
}