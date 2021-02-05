pipeline{
    agent any
    environment {
        HOME = '.'
    }
    stages {
        stage('Build') {
            steps {
                sh 'echo "Hello World" step 2'
                sh 'echo "Hello World" step 3'
            }
        }
    }
    post{
        always{
            echo "ok ====++++always++++===="
        }
        success{
            echo "ok ====++++only when successful++++===="
        }
        failure{
            echo "ok ====++++only when failed++++===="
        }
    }
}