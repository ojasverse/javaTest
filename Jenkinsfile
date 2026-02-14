pipeline {
    agent any

    triggers {
        cron('H/5 * * * *')
        pollSCM('H/1 * * * *')
    }

    stages {

        stage('Clone Repository') {
            steps {
                echo "Cloning repository..."
            }
        }

        stage('Build') {
            steps {
                echo "Building project..."
            }
        }

        stage('Echo Build Status') {
            steps {
                echo "Build successful!"
            }
        }

        stage('Archive Artifacts') {
            steps {
                archiveArtifacts artifacts: '**/*', fingerprint: true
            }
        }
    }
}
