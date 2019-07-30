pipeline {
    agent {
        docker { image 'node:12-alpine' }
    }
    environment {
        HOME = '.'
    }
    stages {
        stage('build') {
            steps {
                sh 'newgrp docker'
                sh 'npm install'
            }
        }
        stage('test') {
            steps {
                sh 'npm test'
            }
        }
        stage('deploy') {
            steps {
                sh 'echo deploying application'
            }
        }
    }
}

