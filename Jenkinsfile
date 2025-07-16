pipeline {
      agent any 
      environment {
        SONAR_SERVICE = "sivadevi2"
      }
       tools {
        maven 'maven-3.8.9'
       }
        stages{
            stage('build'){
                steps {
                    echo "hello world"
                    sh 'mvn package'
                }
            }
            stage('sonar Analysis') {
                steps {
                    withSonarQubeEnv("${SONAR_SERVICE}"){
                        sh 'mvn sonar:sonar -Dsonar.projectKey=sai'
                    }
                }
            }
    }
}
