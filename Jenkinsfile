pipeline {
    agent any
    tools{
        maven 'local maven'
    }
    stages{
        stage ('build'){
            steps{
                sh 'mvn clean package'
                sh "/usr/bin/docker build . -t tomcatwebapp:${env.BUILD_ID}"
        
            }
        }
    }

  
}