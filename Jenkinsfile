pipeline {
    agent any

    stages {

       stage('Clone') {
    steps {
        git 'https://github.com/chander2109/aws-jenkins-eks-project.git'
    }
}

        stage('Build Image') {
            steps {
                sh 'docker build -t myapp:v1 .'
            }
        }

        stage('Deploy') {
            steps {
                sh 'kubectl apply -f deployment.yaml'
                sh 'kubectl apply -f service.yaml'
            }
        }
    }
}
