pipeline {

    agent any

    tools {
        maven 'Maven'
    }

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                url: 'https://github.com/sgayatrijadhav-hub/GayatriSelenium2.git'
            }
        }

        stage('Compile') {
            steps {
                sh 'mvn compile'
            }
        }

        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }

        stage('Package') {
            steps {
                sh 'mvn package'
            }
        }

        stage('Verify Files') {
            steps {
                sh 'ls'
            }
        }

        stage('Open Google') {
            steps {
                echo 'Google Link: https://www.google.com'
                sh 'export DISPLAY=:0 && mvn exec:java -Dexec.mainClass="com.example.App"'
            }
        }

        stage('Complete') {
            steps {
                echo 'Pipeline Completed Successfully'
            }
        }
    }
}
