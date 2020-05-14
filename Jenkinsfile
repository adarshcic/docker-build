pipeline {

    agent any

    stages {
        stage('Clone repository') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {
                script {
                    def app = docker.build("mytest:latest")
                    app.push()
                }
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
