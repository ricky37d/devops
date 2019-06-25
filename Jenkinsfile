pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
      checkout scm      
      }
    }
      stage('Build') {
        steps {
         sh 'mvn clean compile' 
         }
      }
      stage('Test') {
        steps {
         sh 'mvn test'
        }
      }
      
      }
    }
