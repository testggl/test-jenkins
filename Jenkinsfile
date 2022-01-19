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
                emailext body: "${DEFAULT_CONTENT}", subject: "${DEFAULT_SUBJECT}", to: "testemailggl9@gmail.com", from: "Jenkins"
            }
        }
    }
}