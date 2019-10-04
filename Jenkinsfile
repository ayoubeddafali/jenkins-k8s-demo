pipeline {
  agent {
    kubernetes {
      yamlFile 'KubernetesPod.yaml'
    }
  }
  stages {

    stage('Checkout') {
      steps {
        container('maven') {
          checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/ayoubensalem/DockerizedENV-Project.git']]])
        }
      }
    }
    stage('Compile') {
      steps {
        container('maven') {
          sh 'mvn compiler:compile'
        }
      }
    }

    stage('Tests') {
      steps {
        container('maven') {
          sh 'mvn surefire:test'
        }
      }
    }

    stage('Package') {
      steps {
        container('maven') {
          sh 'mvn jar:jar'
          sh "sleep 30m"
        }
      }
    }
  }
}
