pipeline {
       agent any
       environment{
            mvnHome = tool name: 'maven-3.8.5', type: 'maven'
            workspace=pwd()
       }
       stages {
           stage("Tools initialization") {
               steps {
                   sh "mvn --version"
                   sh "java -version"
               }
           }
           stage("Checkout Code") {
               steps {
                   git branch: 'demo-decl-5',
                       url: "https://github.com/mandar-git/demo-jenkins-pipelines.git"
               }
           }
           stage("Cleaning workspace") {
               steps {
                   sh "mvn clean"
               }
           }
           stage("Running Testcase") {
              steps {
                   sh "mvn test"
               }
           }
           stage("Packing Application") {
               steps {
                   sh "mvn package -DskipTests"
               }
           }
       }
 }
