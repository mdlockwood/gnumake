pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        ws(dir: '/tmp/workspace') {
          git(url: 'http://github.com/mdlockwood/gnumake.git', branch: 'master')
        }
        
        sh 'tar xfv make-3.81.tar.gz'
        sh 'configure --prefix=/usr/local'
        sh 'make'
        sh 'make install'
        sh 'ls -l /usr/local/bin'
      }
    }
  }
}