pipeline {
  agent any
  stages {
    stage('Git checkout') {
      steps {
        checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'gitaccess', url: 'https://github.com/Harikiran9100/myweb.git']])
      }
    }
    stage('Building the image') {
      steps {
        sh """
        docker build -t "javaapplication" .
        """
      }
    }
  }
}
