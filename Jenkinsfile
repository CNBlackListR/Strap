pipeline {
  agent {
    docker {
      image 'gradle:4.10.2-jdk11'
    }

  }
  stages {
    stage('build') {
      steps {
        sh '''

gradle shadowJar'''
        archiveArtifacts(artifacts: 'build/libs/*.jar', fingerprint: true)
      }
    }
  }
}