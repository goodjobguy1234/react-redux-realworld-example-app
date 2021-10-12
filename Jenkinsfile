pipeline {
    agent {
        docker {
            image 'mrts/docker-python-nodejs-google-chrome'
            args '-p 8080:8080'
        }
    }

    environment {
        HOME="."
    }

    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }

        stage('Deploy') {
            steps {
                sh 'npm start'
            }
        }
    }
}