pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
      checkout scm      
      }
      stage('print name') {
        steps {
         sh 'echo "Karan"' 
         }
      stage('print lastname') {
        steps {
         sh 'echo "Singh"' 
        }
      }
      
      }
    }
