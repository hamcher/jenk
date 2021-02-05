pipeline{
    agent any
    environment {
        HOME = '.'
        MAIN_URL = 'https://testenv.com'
    }
    stages {
        stage('Build') {
            steps {
                echo "step 1 GIT_COMMIT: ${GIT_COMMIT} "
                echo "step 2 GIT_PREVIOUS_SUCCESSFUL_COMMIT: ${GIT_PREVIOUS_SUCCESSFUL_COMMIT} "
                echo "step 4 GIT_COMMITTER_NAME: ${GIT_COMMITTER_NAME} "
                echo "step 5 GIT_COMMITTER_EMAIL: ${GIT_COMMITTER_EMAIL} "
                echo "step 6 GIT_AUTHOR_EMAIL: ${GIT_AUTHOR_EMAIL} "
                echo "step 7 GIT_COMMITTER_EMAIL: ${GIT_COMMITTER_EMAIL} "

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