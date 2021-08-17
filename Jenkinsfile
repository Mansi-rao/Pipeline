pipeline {
  agent any
  stages {
    stage('Compile') {
      steps {
        withMaven(jdk: 'jdk11', maven: 'maven3') {
          sh 'mvn compile'
        }

      }
    }

    stage('Test') {
      steps {
        withMaven(jdk: 'jdk11', maven: 'maven3') {
          sh 'mvn test'
        }

      }
    }

    stage('Publish result') {
      steps {
        withMaven(jdk: 'jdk11', maven: 'maven3') {
          junit 'target/**.xml'
        }

      }
    }

  }
  environment {
    AUTHOR = 'Mansi'
  }
}