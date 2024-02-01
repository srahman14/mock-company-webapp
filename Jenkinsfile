pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                script {
                    checkout scm
                }
            }
        }
        
        stage('Build') {
            steps {
                script {
                    sh './gradlew assemble'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './gradlew test'
                }
            }
        }
        
    }
    
    post {
        success {
            echo 'Pipeline succeeded! You can add more actions here.'
        }
        failure {
            echo 'Pipeline failed! You can add more actions here.'
        }
    }
}
