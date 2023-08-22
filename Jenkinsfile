pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                bat'mvn -version'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}