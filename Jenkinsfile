pipeline {
    agent any

   

    stages {
        

        stage('Build') {
            steps {
                script {
                    echo 'Building...'

                     if (env.BRANCH_NAME == 'master') {
                        echo 'Running additional steps for the master branch...'
                        
                    } else if (env.BRANCH_NAME == 'develop') {
                        echo 'Running additional steps for the develop branch...'
                       
                    } else {
                        echo 'Running default steps for other branches...'
                        
                    }

                    // Common build steps
                    echo "Branch selected...."
                }
            }
        }

      
    }

    post {
        always {
            echo 'i am post section'
        }
        success {
            echo 'Pipeline succeeded!'
        }
        failure {
            echo 'Pipeline failed!'      }    }

}
