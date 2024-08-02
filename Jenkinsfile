pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/ozgenur19/Game2048.git'
            }
        }

        stage('Build') {
            steps {
               bat 'echo "Running build..."'
               
            }
        }

        stage('Test') {
            steps {
                bat 'echo "Running testing..."'
                
                
               
            }
        }

        stage('Deploy') {
            steps {
             
            bat 'docker build -t my-app-image .'
            bat 'docker run -d -p 8080:8080 --name my-app-container my-app-image'
                
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
