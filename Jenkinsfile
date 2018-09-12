pipeline {
    agent any
    tools{
        maven 'local maven'
        docker 'local docker'
    }
    stages{
        stage ('build'){
            steps{
                sh 'mvn clean package'
                sh 'whoami'
                sh 'echo $PATH'
                sh "docker build . -t tomcatwebapp:${env.BUILD_ID}"
        
            }
        }
    }

  
}