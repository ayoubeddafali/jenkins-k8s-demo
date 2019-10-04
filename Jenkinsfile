pipeline {
  agent {
    kubernetes {
      yamlFile 'KubernetesPod.yaml'
    }
  }
  stages {
    stage('Compile') {
      steps {
        container('maven') {
          sh 'mvn compile'
        }
      }
    }

    stage('Tests') {
      steps {
        container('maven') {
          sh 'mvn test'
        }
      }
    }

    stage('Package') {
      steps {
        container('maven') {
          sh 'mvn package'
        }
      }
    }
  }
}
