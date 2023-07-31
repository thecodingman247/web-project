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
            input message: "Archive Artifacts?", ok: 'Archive'
            archiveArtifacts artifacts: 'build/**/*', fingerprint: true
        }
        failure {
            echo "Build failed, no artifacts will be archived."
        }
    }
}
