pipeline {
    agent { docker { image 'python:3.10.1-alpine' } }
    stages {
        stage('Check branch') {
            steps {
                echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL} using branch: " + env.BRANCH_NAME
            }
        }
        stage('build') {
            steps {
                sh 'python --version'
            }
        }
        stage('execute tests') {
            steps {
                sh 'python test_sum_unittest.py'
            }
        }
    }
}