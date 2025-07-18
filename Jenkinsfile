pipeline {
    agent any
    tools {
        maven 'maven-3.8.9'
    }
    stages {
        stage('bulid') {
            steps {
                echo 'building the project...'
                sh 'make build'
                sh 'mvn install'
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
