node{
// demo3
   stage('SCM Checkout'){
     git branch: 'demo4', url: 'https://github.com/mandar-git/demo-jenkins-pipelines'
   }
   stage('Compile-Package'){
     def mvnHome = tool name: 'maven-3.8.5', type: 'maven'
      sh "${mvnHome}/bin/mvn package"
   }
   stage('Cleanup'){
      cleanWs()
 }
}
