pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        git(url: 'https://github.com/jaipalreddyk/hello-world.git', branch: 'master')
      }
    }
    stage('Compile') {
      parallel {
        stage('Compile') {
          steps {
            sh '''withMaven(maven : \'Maven\')
 {
                    sh \'mvn package\'
        
            }'''
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