pipeline {
  agent any
    tools {
    maven "Maven3" 
     }
    triggers {
            pollSCM("* * * * *")
    }
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
