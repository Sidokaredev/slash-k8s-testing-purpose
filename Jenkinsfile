pipeline {
    agent{
        label 'jnlp-with-docker'
    }
    stages {
        stage(name: 'build') {
            steps {
                echo 'Hello World'
            }
        }
        stage(name: 'staging') {
            steps{
                step {
                    sh(script: 'kubectl get pods -A')
                }
            }
        }
    }
}
