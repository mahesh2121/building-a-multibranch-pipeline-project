

pipeline {
    agent {
        docker {
            image 'node:18.18.0-alpine3.18'
            args '-v /run/containerd/containerd.sock:/run/containerd/containerd.sock -p 3000:3000 -p 5000:5000'
        }
    }
    environment {
        CI = 'true'
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                sh './jenkins/scripts/test.sh'
            }
        }
    }
}





     
           
            
        
    

