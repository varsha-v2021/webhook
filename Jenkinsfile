pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Checking Java application'
                bat 'javac Main.java'
            }
        }

        stage('Test') {
            steps {
                echo 'Executing automated tests'
                bat 'java Test'
            }
        }

        stage('Run Application') {
            steps {
                bat 'java Main'
            }
        }
    }

    post {
        success {
            echo 'CI Pipeline completed successfully'
        }

        failure {
            echo 'CI Pipeline failed'
        }
    }
}
