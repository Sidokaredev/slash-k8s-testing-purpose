pipeline {
    agent{
        label 'jnlp-with-docker'
    }
    stages {
        stage('build') {
            steps {
                echo 'Hello World'
            }
        }
        stage('staging') {
            steps {
                withKubeConfig(
                    credentialsId: 'private-k8s-certificate',
                    serverUrl: 'https://kubernetes.default.svc.cluster.local',
                    clusterName: 'private-k8s',
                    contextName: 'vbox-k8s'
                ) {
                    sh '''
                        echo "viewing kubernetes config file ..."
                        kubectl config view

                        echo "listing pods available ..."
                        kubectl get pods -A
                    '''
                }
            }
        }
    }
}
