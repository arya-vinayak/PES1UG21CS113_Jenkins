pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    // Replace 'main.cpp' with the correct name of your C++ file
                    sh 'g++ crazy.cpp -o output'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    sh './non_output'
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }
    post {
        failure {
            error 'Pipeline failed'
        }
    }
}