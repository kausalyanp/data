pipeline {
    agent any

    tools {
        maven 'Maven_3.6.3' // Define the Maven tool version
    }

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/your-username/jenkins-maven-example.git', branch: 'master'
            }
        }

        stage('Build') {
            steps {
                script {
                    echo 'Building the application...'
                    sh 'mvn clean install'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    echo 'Running unit tests...'
                    sh 'mvn test'
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    echo 'Deploying the application...'
                    // Add your deployment steps here
                }
            }
        }
    }

    post {
        success {
            echo 'Pipeline succeeded!'
        }

        failure {
            echo 'Pipeline failed!'
        }
    }
}

