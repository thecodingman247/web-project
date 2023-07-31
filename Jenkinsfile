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
        stage('build') {
            steps {
                sh 'npm run build'
            }
        }
    }

    post {
        success {
             archiveArtifacts artifacts: 'build/**/*'
        }
    }
}
