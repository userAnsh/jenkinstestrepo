pipeline {
    agent any
    stages {
        stage('Example') {
            steps {
                echo 'Hello World'
                
                echo "${JOB_NAME} - Build #${env.BUILD_NUMBER} ${currentBuild.result}"
                echo "${GIT_COMMIT}"
                echo "${env.GIT_COMMITTER_EMAIL}"
                echo "${env.GIT_COMMITTER_NAME}"
                echo "${env.GIT_AUTHOR_EMAIL}"
                echo "${env.GIT_AUTHOR_NAME}"   
                echo "${env.GIT_USER}"
                echo 'How many did u got'
                echo 'names printed'
            }
        }
    }
    post { 
        always { 
            echo 'I will always say Hello again!'
          
        }
        success {
            echo ' Job completed successfully'
        }
        
        failure {
            echo ' Job failed'
        }
        
        changed {
            echo ' Something is changed'
        }
    }
}