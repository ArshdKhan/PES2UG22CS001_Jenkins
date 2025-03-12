pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ main.cpp -o main_exec'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './main_exec'
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
