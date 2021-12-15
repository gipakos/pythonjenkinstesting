pipeline {
    agent { docker { image 'python:3.10.1-alpine' } }
    stages {
        stage('Check branch') {
            echo "Using branch: ${env.BRANCH_NAME}"
        }
        stage('build') {
            steps {
                sh 'python --version'
            }
        }
    }
}