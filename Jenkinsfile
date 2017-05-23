pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        withMaven(maven: 'Maven 3.5.0') {
          sh 'mvn package'
        }
        
      }
    }
  }
}