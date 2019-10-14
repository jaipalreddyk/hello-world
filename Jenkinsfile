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
            sh ''' sh \'mvn package\'
withMaven(maven : \'Maven\')
 
                   
        
            '''
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