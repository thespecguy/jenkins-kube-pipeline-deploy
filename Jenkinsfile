pipeline {
agent any
  
  parameters {
    booleanParam(name: "isDeployPod" ,defaultValue: true)
  }
  stages {
    stage('abc') {
      when {
        expression {
          params.isDeployPod
        }
      }
      steps {
        sh "kubectl apply -f deploy.yml --kubeconfig /admin.conf"
      }
    }
  }
  post {
    success {
      echo "All Good"
    }
    failure {
      echo "Something failed"
    }
    always {
       echo "Always"
    }
  }
}
