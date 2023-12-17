pipeline {
    agent any


    options {
        buildDiscarder(logRotator(numToKeepStr: '10'))
        disableConcurrentBuilds()
    }

    


        stage('Set Environment and Run Specific Steps') {
            steps {
                script {
                    
                    def currentBranch = env.BRANCH_NAME
                     echo 'Common steps for all branches...'
                    

                       switch (currentBranch) {
                        case 'master':
                            echo 'Running steps for the master branch...'
	                         break
                            

                        case 'main':
                            echo 'Running steps for the Main branch...'
                          	break
                            

                        default:
                            echo "Running default steps for branch: ${currentBranch}"
				break                    }                }            }        }

        stage('Build') {
            steps {
                script {
                    echo 'build'                }            }        } }




    post {
        always {
            echo 'PostAction'
        }
        success {
            echo 'Pipeline succeeded!'
            // Additional steps for success
        }
        failure {
            echo 'Pipeline failed!'
            // Additional steps for failure        }     }
}
