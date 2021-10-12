pipeline {
    agent any {
        image ''
        args '-p 4100:4100'
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