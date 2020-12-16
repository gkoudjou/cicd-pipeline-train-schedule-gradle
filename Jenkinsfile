pipeline {

  agent any;
  
  stages {
    stage('Build') {
      steps {
          sh '''
          ./gradlew build
          '''
      }
    }
  }
  
  post {
    success {
        archiveArtifacts artifacts: 'dist/*.zip', fingerprint: true
    }
  }

}
