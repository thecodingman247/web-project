pipeline {
    agent {label 'slave1'}

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
