pipeline{
   agent any
   
   environment{
      mvnHome = tool name: 'maven-3.8.5', type: 'maven'
      dockerHome = tool 'myDocker'
      PATH = "${dockerHome}/bin:${PATH}"
   }
   stages {
      stage("Git Checkout"){
         steps{
            git branch: 'demo-decl-2', credentialsId: 'mandar_git', url: 'https://github.com/mandar-git/demo-jenkins-pipelines.git'
         }
      }
      stage('Maven Build'){
         steps{
            sh "${mvnHome}/bin/mvn clean package"
         }
      }
      stage('Build Docker Image'){
         steps{
            sh 'docker build -f /var/lib/jenkins/workspace/decl-pipeline-3/pipeline/Dockerfile-t mandar1983/my-py-webapp:latest ./var/lib/jenkins/workspace/decl-pipeline-3/pipeline'
         }
      }
       stage('Clean Workspace'){
         steps{
            cleanWs()
         }
      }
   }
}
