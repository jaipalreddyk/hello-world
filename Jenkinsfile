pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        git(url: 'https://github.com/jaipalreddyk/ecommerce.git', branch: 'master')
      }
    }
    stage('Compile') {
      parallel {
        stage('Compile') {
          steps {
            sh 'sh \'mvn clean\''
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