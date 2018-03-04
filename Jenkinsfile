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
    stage('promoto to QA') {
      steps {
        sh 'oc tag todo/todolist:latest todo/todolist:promotoToQA'
      }
    }
  }
}