pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/ilyas111111111/Devops-projet.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                script {
                    sh 'docker build -t html-project .'
                }
            }
        }

        stage('Run Container') {
            steps {
                script {
                    sh 'docker run -d -p 8080:80 html-project'
                }
            }
        }
    }
}
