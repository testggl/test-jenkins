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
                emailext body: "${env.DEFAULT_CONTENT}", subject: "${env.DEFAULT_SUBJECT}", to: "testemailggl9@gmail.com", from: "Jenkins"
            }
        }
    }
}