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
                sh 'podman build -t jenkins-lab .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'podman run -d --name jenkins-lab jenkins-lab'
            }
        }
    }
}
