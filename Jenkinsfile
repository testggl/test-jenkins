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
                emailext body: '$PROJECT_NAME - Build # $BUILD_NUMBER - $BUILD_STATUS', subject: 'Jenkins Job Result', to: 'testemailggl9@gmail.com', from: 'Jenkins'
            }
        }
    }
}