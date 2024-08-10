pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/djouekan/hooks.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                sh 'npm test'
            }
        }

        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }
    }

    post {
        always {
            sh 'npm run start:dev'
        }
    }
}
