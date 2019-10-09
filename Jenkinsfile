pipeline {
  agent {
    node {
      label 'master'
    }

  }
  stages {
    stage('checkout') {
      steps {
        sh 'sh \'https://github.com/jaipalreddyk/hello-world.git\''
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