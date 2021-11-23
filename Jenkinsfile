pipeline {
    agent none
    stages {
        stage('Build') { 
            agent {
            node {
                sh 'python -m py_compile sources/add2vals.py sources/calc.py' 
                stash(name: 'compiled-results', includes: 'sources/*.py*') 
            }
          }
        }
    }
}
