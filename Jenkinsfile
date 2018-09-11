pipeline {
    agent any
    tools{
        maven 'local maven'
    }
    stages{
        stage ('build'){
            steps{
                sh 'mvn clean package'
                sh 'echo $PATH'
                sh "docker build . -t tomcatwebapp:${env.BUILD_ID}"
        
            }
        }
    }

  
}