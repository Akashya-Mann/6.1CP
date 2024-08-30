pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the code...'
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo 'Running unit and integration tests...'
            }
        }
        stage('Code Analysis') {
            steps {
                echo 'Analyzing the code...'
            }
        }
        stage('Security Scan') {
            steps {
                echo 'Performing security scan...'
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo 'Deploying to staging server...'
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo 'Running integration tests on staging...'
            }
        }
        stage('Deploy to Production') {
            steps {
                echo 'Deploying to production server...'
            }
        }
    }
    post {
        success {
            echo 'Pipeline succeeded!'
            mail to: 'whatnutrunt@gmail.com',
                 subject: "Build Success: ${env.JOB_NAME} #${env.BUILD_NUMBER}",
                 body: "Good news! The build was successful.\nCheck console output at ${env.BUILD_URL}."
        }
        failure {
            echo 'Pipeline failed!'
            mail to: 'whatnutrunt@gmail.com',
                 subject: "Build Failure: ${env.JOB_NAME} #${env.BUILD_NUMBER}",
                 body: "Unfortunately, the build has failed.\nCheck console output at ${env.BUILD_URL}."
        }
    }
}
