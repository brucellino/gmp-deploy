pipeline {
  agent none
  environment {
    ARCH = 'x86_64'
    SITE = 'generic'
    NAME = 'gmp'
  }
  stages {
    stage('build') {
      parallel {
        stage('build 6.1.2 on centos6') {
          environment {
            OS = 'centos6'
            VERSION = '6.1.2'
          }
          agent { label "centos6" }
          steps {
            sh 'echo $SITE $NAME $OS $ARCH $VERSION'
            sh './build.sh'
          }
        }
        stage('build 6.1.0 on centos6') {
          environment {
            OS = 'centos6'
            VERSION = '6.1.0'
          }
          agent { label "centos6" }
          steps {
            sh 'echo $SITE $NAME $OS $ARCH $VERSION'
            sh './build.sh'
          }
        }
        stage('build 6.1.2 on centos7') {
          environment {
            OS = 'centos7'
            VERSION = '6.1.2'
          }
          agent { label "centos7" }
          steps {
            sh 'echo $SITE $NAME $OS $ARCH $VERSION'
            sh './build.sh'
          }
        }
        stage('build 6.1.0 on centos7') {
          environment {
            OS = 'centos7'
            VERSION = '6.1.0'
          }
          agent { label "centos7" }
          steps {
            sh 'echo $SITE $NAME $OS $ARCH $VERSION'
            sh './build.sh'
          }
        }
        stage('build 6.1.2 on ubuntu 1404') {
          environment {
            OS = 'u1404'
            VERSION = '6.1.2'
          }
          agent { label "u1404" }
          steps {
            sh 'echo $SITE $NAME $OS $ARCH $VERSION'
            sh './build.sh'
          }
        }
        stage('build 6.1.0 on ubuntu 1404') {
          environment {
            OS = 'u1404'
            VERSION = '6.1.0'
          }
          agent { label "u1404" }
          steps {
            sh 'echo $SITE $NAME $OS $ARCH $VERSION'
            sh './build.sh'
          }
        }
        stage('build 6.1.2 on ubuntu 1610') {
          environment {
            OS = 'centos6'
            VERSION = '6.1.2'
          }
          agent { label "u1610" }
          steps {
            sh 'echo $SITE $NAME $OS $ARCH $VERSION'
            sh './build.sh'
          }
        }
        stage('build 6.1.0 on ubuntu 1610') {
          environment {
            OS = 'u1610'
            VERSION = '6.1.0'
          }
          agent { label "u1610" }
          steps {
            sh 'echo $SITE $NAME $OS $ARCH $VERSION'
            sh './build.sh'
          }
        }
      }
    }
  }
}