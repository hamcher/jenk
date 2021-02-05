pipeline{
    agent any
    environment {
        HOME = '.'
        MAIN_URL = 'https://testenv.com'
    }
    stages {
        stage('Build') {
            steps {
                echo "step 1 ====++++ ${MAIN_URL} ++++===="
            }
        }
    }
    post{
        always{
            echo "ok ====++++always++++==== ${MAIN_URL}"
        }
        success{
            echo "ok ====++++only when successful++++===="
        }
        failure{
            echo "ok ====++++only when failed++++===="
        }
    }
}