pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ hello.cpp -o hello_exec'
            }
        }
        stage('Test') {
            steps {
                sh './hello_exec'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deployment successful!'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}

