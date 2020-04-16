node {
    
    stage('Checkout Source') {
        git 'https://github.com/asarutv/playjenkins'
    }

    stage("Deploy To Kuberates Cluster"){
        sh 'kubectl apply -f myweb.yaml'
    }
}
