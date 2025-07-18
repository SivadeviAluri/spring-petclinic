pipeline {
    agent any
    stages {
        stage('bulid') {
            steps {
                echo 'building the project...'
                sh 'make build'
            }
        }
        stage('test') {
            steps {
                echo 'running tests...'
                sh 'make test'            
            }
        }
          stage('deploy') {
        when {branch 'main'}
        steps {
            echo 'deploying to production..'
            sh 'make deploy' 
            
        }    
          }   
    }
}
