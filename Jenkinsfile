pipeline {
  agent any
  stages {

    stage('Debug') {
      steps {
        script {
          println(scm.GIT_BRANCH)
          println(scm.getRepositories())
        }
      }
    }
  }
}
