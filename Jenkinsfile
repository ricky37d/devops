pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        checkout scm
      }
    }
    stage('Clean') {
      sh 'chmod +x mvnw'
     sh './mvnw clean' 
    }
    stage('Compile') {
      sh './mvnw compile' 
    }
  }
}
