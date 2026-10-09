pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'git@github.com:Abdul5412/new-cicd-project.git'
            }
        }

        stage('Build') {
            steps {
                sh 'docker build -t new-cicd-project .'
            }
        }

        stage('Test') {
            steps {
                sh 'docker image inspect new-cicd-project'
                echo 'Build and test successful!'
            }
        }
    }
}
