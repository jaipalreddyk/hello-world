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
            sh '''echo "PATH = ${PATH}"
echo "M2_HOME = ${M2_HOME}"
sh \'mvn package\''''
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