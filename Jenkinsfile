pipeline{
    agent any
    environment {
        HOME = '.'
    }
    stages {
        stage('build') {
            steps {
                sh 'npm -v'
                sh 'echo "Hello World" step 2'
                sh 'echo "Hello World" step 3'
            }
        }
    }
}