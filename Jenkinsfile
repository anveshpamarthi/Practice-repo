pipeline {
  agent any
  stages {
    stage('scm') {
      steps {
        git(url: 'https://github.com/anveshpamarthi/java_src.git', branch: 'master', poll: true)
      }
    }
    stage('build') {
      steps {
        sh 'mvn clean compile package'
      }
    }
    stage('deploy') {
      steps {
        sh 'mvn deploy'
      }
    }
  }
}