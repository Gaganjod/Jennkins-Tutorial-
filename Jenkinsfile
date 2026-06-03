pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                bat 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }

        stage('Docker Build') {
            steps {
                bat 'docker build -t studentapp .'
            }
        }

        stage('Docker Push') {
            steps {
                bat 'docker tag studentapp gagan/studentapp:latest'
                bat 'docker push gagan/studentapp:latest'
            }
        }

    }
}