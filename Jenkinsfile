pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        git(url: 'https://github.com/mdlockwood/gnumake.git', branch: 'master')
        sh 'tar xfv make-3.8.1.tar.gz'
        sh 'configure'
        sh 'make'
      }
    }
  }
}