pipeline {
    agent any

    triggers {
        pollSCM('H/2 * * * *')
    }

    stages {
        stage('Checkout') {
            steps {
                echo 'Checkout stage: Getting source code from GitHub'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Jenkins SCM polling test.'
            }
        }

        stage('Test') {
            steps {
                echo 'Test stage: Running application tests'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploy stage: Deployment completed successfully'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed. Check the Console Output.'
        }
    }
}
