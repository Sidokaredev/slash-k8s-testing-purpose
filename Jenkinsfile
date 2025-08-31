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
                sh(script: 'kubectl get pods -A')
            }
        }
    }
}
