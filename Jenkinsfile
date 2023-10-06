pipeline {
    agent any

    stages {
        stage ('Build Image') {
            steps {
                script {
                //    dockerapp = docker.build("andrebaldo/api-produto:v1", '-f ./src/Dockerfile ./src') 
                }                
            }
        }

        stage ('Push Image') {
            steps {
                //script {
                 //   docker.withRegistry('https://registry.hub.docker.com', 'dockerhub') {
                  //      dockerapp.push('latest')
                   //     dockerapp.push("v1")
                   // }
                }
            }
        }

        stage ('Deploy Kubernetes') {
            environment {
                tag_version = "v1"
            }
            steps {
               
                sh 'kubectl apply -f ./k8s/deployment.yaml'
                
            }
        }
    }
}