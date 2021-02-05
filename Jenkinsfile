pipeline{
    agent any
    environment {
        HOME = '.'
        MAIN_URL = 'https://testenv.com'
    }
    stages {
        stage("Test"){
            steps{
                echo "====++++executing Test++++===="
            }
        }
        stage('Build') {
            steps {
                echo "step 1 GIT_COMMIT: ${GIT_COMMIT} "

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