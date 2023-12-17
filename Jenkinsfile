pipeline {
    agent any

    environment {
        // Accessing system environment variables
        GIT_BRANCH = env.BRANCH_NAME
        BUILD_NUMBER = env.BUILD_NUMBER
        JOB_NAME = env.JOB_NAME
        // Add more variables as needed
    }

    stages {
        stage('Print Environment Variables') {
            steps {
                script {
                    // Printing system environment variables
                    echo "GIT_BRANCH: ${GIT_BRANCH}"
                    echo "BUILD_NUMBER: ${BUILD_NUMBER}"
                    echo "JOB_NAME: ${JOB_NAME}"
                    // Add more echo statements as needed
                }
            }
        }

        // Add more stages as needed
    }

    post {
        success {
            // Additional steps for success
        }
        failure {
            // Additional steps for failure
        }
    }
}

