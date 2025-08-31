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
            steps{
                step {
                    sh(script: 'kubectl get pods -A')
                }
            }
        }
    }
}
