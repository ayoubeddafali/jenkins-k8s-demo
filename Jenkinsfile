pipeline {
  agent {
    kubernetes {
      yamlFile 'KubernetesPod.yaml'
    }
  }
  stages {
    stage('Run maven') {
      steps {
        sh "ls"
        sh "hostname"
        container('maven') {
          sh 'ls'
          sh 'hostname'
        }
      }
    }
  }
}
