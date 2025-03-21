pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/YOUR_USERNAME/hello-world.git'
            }
        }
        stage('Build') {
            steps {
                sh 'docker build -t hello-world .'
            }
        }
        stage('Test') {
            steps {
                sh 'docker run --rm hello-world'
            }
        }
        stage('Deploy') {
            steps {
                sh 'docker run -d -p 8080:80 hello-world'
            }
        }
    }
}
