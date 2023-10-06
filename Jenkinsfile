pipeline {
    agent any

        stage ('Deploy Kubernetes') {
       
            steps {
               script{
                    sh 'kubectl apply -f ./k8s/deployment.yaml'
               }
                
                
            }
        }
    }
