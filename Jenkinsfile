pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build Image') {
            steps {
                sh 'docker build -t jenkins-lab .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d --name jenkins-lab jenkins-lab'
            }
        }
    }
}
