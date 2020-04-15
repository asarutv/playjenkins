pipeline {

  agent { label 'kube-pod-front' }

  stages {

    stage('Checkout Source') {
      steps {
        git 'https://github.com/asarutv/playjenkins.git'
      }
    }

    stage('Deploy App') {
      steps {
        script {
          kubernetesDeploy(configs: "myweb.yaml", kubeconfigId: "KUBECONFIG")
        }
      }
    }
 
  }

}
