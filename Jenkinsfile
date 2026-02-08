pipeline {
    agent any

    stages {
        stage('Clone Code') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/JonSOnow/devops-project.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t devops-nginx .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 8084:80 devops-nginx'
            }
        }
    }
}
