pipeline{
    agent any
    environment {
        HOME = '.'
        MAIN_URL = 'https://testenv.com'
    }
    stages {
        stage("Test") {
            agent {
                dockerfile {
                    filename 'Dockerfile'
                    additionalBuildArgs "--build-arg SSH_PR_KEY=\"\$(cat ${SSH_KEY})\""
                    reuseNode true
                }
            }
            steps{
                sh '. /root/.nvm/nvm.sh &&  nvm install && npm -v'
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