pipeline {
  agent any

  stages {
    stage('Checkout') {
      steps {
        checkout scm
      }
    }
  
    stage('Build') {
      steps {
        script {
          def buildNumber = env.BUILD_NUMBER
          sh "mvn clean install -DbuildNumber=$buildNumber"
        }
      }
    }
  }
}
