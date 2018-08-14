pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        ws(dir: '/tmp/workspace') {
          git(url: 'http://github.com/mdlockwood/gnumake.git', branch: 'master')
        }
        
        sh 'ls -l'
        sh 'ls -l /tmp/workspace'
      }
    }
  }
}