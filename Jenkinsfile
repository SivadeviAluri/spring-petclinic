pipeline {
    agent any
    stages {
        tools {
            maven 'mavem-3.8.9'
        }
        stage('bulid') {
            steps {
                echo 'building the project...'
                sh 'make build'
            }
        }
    
    }
}
