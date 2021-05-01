pipeline {
agent any
  stages {
    stage('abc') {
      when {
        expression {
          false
        }
      }
      steps {
        kubernetesDeploy(configs: "deploy.yml", kubeconfigId: "mykubeconfigfile" )
      }
    }
  }
  
}
