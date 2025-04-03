
pipeline {
    agent any
    stages {
        stage('Get Pods') {
            steps {
              script {
                withKubeConfig([credentialsId: 'eks'] ) {
                  sh "kubectl get pod"
                  sh 'kubectl apply -f deployment.yml'     
                }
              }  
            }
         }
     }
}
      
