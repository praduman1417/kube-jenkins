pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                echo "build: hello big world   out there"
                
            }
        }

        stage('Deploy') { 
            steps {
                echo "deploy: hello big world   out there"
            }
        }
        
         stage('Apply Kubernetes files') {
             steps {
                 withKubeConfig([credentialsId: 'kubernetes-dashboard-wsl-ubuntu', serverUrl: 'https://kubernetes.docker.internal:6443']) {
                 sh 'kubectl get ns --all-namespaces'
                               }
             }
  
}
    }
}
