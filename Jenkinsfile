pipeline {
    agent none
    stages {
        stage('Init') {
          agent any
          steps {
            sh "echo Initializing"
          }
        }
        stage('Build Images') {
            parallel {
                stage('Image A') {
                    agent any
                    steps {
                        sh "sleep 1; echo A; sleep 8; echo A"
                    }
                }
                stage('Image B') {
                    agent any
                    steps {
                        sh "echo B; sleep 10; echo B"
                    }
                }
            }
        }
    }
}

