pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh './gradlew assemble'
            }
        }
        stage('Test') {
            steps {
                sh './gradlew test'
            }
        }
        stage('Sending Email') {
            steps {
                emailext attachLog: true, body: 'Build and Test was succeeded', subject: 'Jenkins Job Result', to: 'testemailggl9@gmail.com'
            }
        }
    }
}