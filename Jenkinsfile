pipeline {
  agent any
  stages {
    stage('Compile') {
      steps {
        withMaven(jdk: 'jdk11', maven: 'maven3') {
          sh 'sh \'mvn compile\''
        }

      }
    }

  }
  environment {
    AUTHOR = 'Mansi'
  }
}