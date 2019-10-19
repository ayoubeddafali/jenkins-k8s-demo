pipeline {
  agent any
  stages {

    stage('Checkout') {
      steps {
        container('maven') {
          checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/ayoubensalem/DockerizedENV-Project.git']]])
        }
      }
    }

    stage('Debug') {
      steps {
          sh 'env'
      }
    }
  }
}
