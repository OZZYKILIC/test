pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                bat 'mvn compile'
                if (currentBuild.currentResult == 'FAILURE') {
                  step([$class: 'Mailer', notifyEveryUnstableBuild: true, recipients: "ozan.kilic@outlook.com", sendToIndividuals: true])
                }
            }
        }
        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}