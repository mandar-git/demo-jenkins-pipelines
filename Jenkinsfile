#!groovy

pipeline {
  agent any  
   environment{
      mvnHome = tool name: 'maven-3.8.5', type: 'maven'
      dockerHome = tool 'myDocker'
      PATH = "${dockerHome}/bin:${PATH}"
   }
  stages {
    stage('Maven Install') {
      agent {
        docker {
          image 'maven:3.5.0'
        }
      }
      steps {
        sh 'mvn clean install'
      }
    }
    stage('Docker Build') {
      agent {
      docker {
          image 'python:3.8-slim'
        }
      }
      steps {
        sh 'docker build -t mandar1983/my-pyweb-app:latest .'
      }
    }
  }
}
