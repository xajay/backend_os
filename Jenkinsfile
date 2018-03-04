pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'mvn clean package'
      }
    }
  }
  environment {
    maven = 'maven'
  }
}