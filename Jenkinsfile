pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Auto Building.. with ${GIT_AUTHOR_NAME}'
            }
        }
        stage('Test') {
            when { 
                expression {
                    BRANCH_NAME == 'main'
                }
            }
            steps {
                echo 'Auto Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Auto Deploying.... with ${GIT_AUTHOR_EMAIL}'
            }
        }
    }
     post {
        always {
            echo "ALWAYS"
        }
        success {
            echo "SUCCCESS"
        }
        failure {
            echo "FAILURE"
        }
    }
            
}
