pipeline {
    agent none        
    stages {
        agent {
            docker {
                image 'python:2-alpine'
            }
        }
        stage('Build') {
            steps {
                sh 'echo $PATH'
                sh 'python -m py_compile sources/add2vals.py sources/calc.py'
                stash(name: 'compiled-results', includes: 'sources/*.py*')
            }
        }
        
    }
}
