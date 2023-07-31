pipeline {
    agent any

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

    post {
        success {
            archiveArtifacts artifacts: '**/*'
        }
    }
}
