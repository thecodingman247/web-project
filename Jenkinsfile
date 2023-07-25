pipeline {
    agent {label 'slave'}

    stages {
        stage('Init') {
            steps {
                sh 'npm i'
            }
        }
        stage('Test') {
            steps {
                sh 'npm run test -- --watchAll=false'
            }
        }
    }
}
