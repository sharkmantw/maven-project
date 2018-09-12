pipeline {
    agent any
    tools{
        maven 'local maven'
    }
    stages{
        stage ('build'){
            steps{
                sh 'mvn clean package'
                sh 'whoami'
                sh 'echo $PATH'
                sh "sudo /usr/local/bin/docker build . -t tomcatwebapp:${env.BUILD_ID}"
        
            }
        }
    }

  
}