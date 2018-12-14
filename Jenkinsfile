pipeline {
  agent {
    docker {
      image 'squidfunk/mkdocs-material'
      args '-v WORKPLACE;/docs --entrypoint bash'
    }

  }
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            sh '''mkdocs build
'''
          }
        }
        stage('test') {
          steps {
            sh 'ls-l_site/'
          }
        }
      }
    }
  }
}