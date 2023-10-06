pipeline {
    agent any

        stage ('Deploy Kubernetes') {
            environment {
                tag_version = "v1"
            }
            steps {
               
                sh 'kubectl apply -f ./k8s/deployment.yaml'
                
            }
        }
    }
