pipeline{
   agent any
   stages {
      stage("Git Checkout"){
         steps{
            git branch: 'demo-decl-2', credentialsId: 'mandar_git', url: 'https://github.com/mandar-git/demo-jenkins-pipelines.git'
         }
      }
      stage('Maven Build'){
         steps{
             mvnHome = tool name: 'maven-3.8.5', type: 'maven'
            sh "${mvnHome}/bin/mvn clean package"
         }
      }
   }
}
