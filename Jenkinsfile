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

        stage('Run Selenium') {
            steps {
                echo 'Google Link: https://www.google.com'
                sh 'mvn exec:java -Dexec.mainClass="com.example.App" || true'
            }
        }

        stage('Complete') {
            steps {
                echo 'Pipeline Completed Successfully'
            }
        }
    }
}
