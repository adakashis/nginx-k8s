pipeline {
    agent any

    stages {
        stage('Deploy Nginx') {
            steps {
                sh '''
                kubectl apply -f deployment.yaml
                kubectl apply -f service.yaml

                kubectl get deployments
                kubectl get pods
                kubectl get svc
                '''
            }
        }
    }
}
