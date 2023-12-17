pipeline {
    agent any

    environment {
        MAVEN_HOME = tool 'Maven'
        PATH = "$MAVEN_HOME/bin:$PATH"
    }

    options {
        buildDiscarder(logRotator(numToKeepStr: '10'))
        disableConcurrentBuilds()
    }

    
        
        stage('Code Coverage') {
            when {
                // Execute this stage only for the 'main' branch
                expression { env.BRANCH_NAME == 'main' }
            }
            steps {
                script {
                    echo "Main branchdone"
                }
            }
        }

        stage('Additional Steps for Feature Branch') {
            when {
                // Execute this stage only for branches starting with 'feature/'
                expression { env.BRANCH_NAME.startsWith('feature/') 
}
            }
            steps {
                script {
                    // Additional steps for feature branches
                    echo 'Running additional steps for feature branch...'
                }
            }
        }
    }

    post {
        always {
            // Publish JUnit test results
            echo "junit '**/target/surefire-reports/*.xml'"
        }
        success {
            // Display a success message
            echo 'Pipeline succeeded!'
        }
        failure {
            // Display a failure message
            echo 'Pipeline failed!'
        }
    }
}
