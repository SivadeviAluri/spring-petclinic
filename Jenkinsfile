pipeline {
      agent any 
       tool {
        maven 'maven-3.8.9'
       }
        stages{
            stage('build'){
                steps {
                    echo "hello world"
                    sh 'mvn package'
                }
            }
    }
}
