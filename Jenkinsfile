pipeline {
    agent any

    environment {
        
        GIT_BRANCH = 'env.BRANCH_NAME'
        BUILD_NUMBER = "env.BUILD_NUMBER"
        JOB_NAME = "env.JOB_NAME"
       
    }

    stages {
        stage('Print Environment Variables') {
            steps {
                script {
                    // Printing system environment variables
                    echo "GIT_BRANCH: ${GIT_BRANCH}"
                    echo "BUILD_NUMBER: ${BUILD_NUMBER}"
                    echo "JOB_NAME: ${JOB_NAME}"
                   
                }
            }
        }

        //
    }

   
}

