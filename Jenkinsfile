node{
// demo2
   stage('SCM Checkout'){
     git 'https://github.com/mandar-git/demo-jenkins-pipelines'
   }
   stage('Compile-Package'){
     def mvnHome = tool name: 'maven-3.8.5', type: 'maven'
      sh "${mvnHome}/bin/mvn package"
   }
}
