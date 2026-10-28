pipeline {
    agent any

    stages {
        stage('Verify') {
            steps {
                sh '''
                pwd
                ls -la
                kubectl version --client
                kubectl get nodes
                '''
            }
        }

        stage('Deploy') {
            steps {
                sh '''
                kubectl apply -f deployment.yaml
                kubectl apply -f service.yaml
                '''
            }
        }
    }
}
