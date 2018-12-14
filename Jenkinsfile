pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''mkdocs build
ls -l_site/
'''
      }
    }
  }
}