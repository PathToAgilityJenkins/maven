pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        dir(path: 'maven') {
          withMaven(maven: 'Maven 3.5.0') {
            sh 'mvn package'
          }
          
        }
        
      }
    }
    stage('Document') {
      steps {
        dir(path: 'maven') {
          withMaven(maven: 'Maven 3.5.0') {
            sh 'mvn site:site'
          }
          
        }
        
      }
    }
  }
}