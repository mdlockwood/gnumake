pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        ws(dir: '/tmp/workspace') {
          git(url: 'http://github.com/mdlockwood/gnumake.git', branch: 'master')
        }
        
        dir(path: '/tmp/workspace') {
          sh 'pwd'
        }
        
        sh 'tar xfv make-3.8.1.tar.gz'
        sh 'configure'
        sh 'make'
      }
    }
  }
}