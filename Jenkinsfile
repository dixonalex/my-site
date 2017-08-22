pipeline {
    agent { docker 'node:6.3' }

    stages {
        stage('Build') {
            steps {
                sh 'npm --version'
                sh './build/build.sh'
            }
        }
        stage('Test') {
            steps {
                echo '(not) Testing..'
            }
        }
        stage('Deploy - Staging') {
            steps {
                echo '(not) Deploying to Staging....'
                //sh './deploy staging'
                //sh './run-smoke-tests'
            }
        }
        stage('Deploy - Production') {
            steps {
                echo 'Deploying to Production....'
                sh './build/deploy.sh'
            }
        }
        stage('Deploy - Production') {
            steps {
                echo 'Cleaning up workspace....'
                sh './build/cleanup.sh'
            }
        }
    }
}