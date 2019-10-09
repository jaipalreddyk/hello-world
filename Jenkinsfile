pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        sh 'git \'https://github.com/jaipalreddyk/hello-world.git\''
      }
    }
    stage('Compile') {
      parallel {
        stage('Compile') {
          steps {
            sh 'sh \'compile\''
          }
        }
        stage('Test') {
          steps {
            sh 'sh \'test\''
          }
        }
      }
    }
  }
}