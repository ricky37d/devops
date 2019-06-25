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
      stage('Test Report') {
          steps {
              script {
                junit '**/surefire-reports/*.xml'
              }
          }
        }
        stage('Sonar Analysis') {
            steps {
                echo 'Sonar Scanner'
                withSonarQubeEnv('sonar67') {
                 sh "mvn sonar:sonar"
                        }
            }
        } 
      }
    }
