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
                bat 'javac App.java'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing Java application'
                bat 'java App'
            }
        }

        stage('Run Application') {
            steps {
                echo 'Running Java application'
                bat 'java App'
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
