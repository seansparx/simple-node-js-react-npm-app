pipeline {
    agent {
        docker {
            image 'node:latest'
            args '-p 3000:3000'
        }
    }
    
    stages {
        stage('Build') {
            steps {
                sh 'echo $PATH'
                sh 'node -v'
                sh 'npm -v'
            }
        }
        
    }
}
