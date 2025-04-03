
pipeline {
    agent any
    stages {
        stage('Get Pods') {
            steps {
              script {
                withkubeConfig([credentialsID: 'eks']) {
                  sh "kubectl get pod"
                  sh 'kubectl apply -f deployment.yml'     
                }
              }  
             }
         }
     }
}
      
