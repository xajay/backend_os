pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'mvn clean package'
      }
    }
    stage('deploy') {
      steps {
        sh 'mvn fabric8:deploy'
      }
    }
  }
  environment {
    maven = 'maven'
  }
}