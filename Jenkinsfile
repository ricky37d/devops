pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        checkout scm
      }
    }
    stage('Clean') {
      steps {
      sh 'chmod +x mvnw'
      }
      steps {
     sh './mvnw clean'
      }
    }
    stage('Compile') {
      steps {
      sh './mvnw compile'
      }
    }
  }
}
