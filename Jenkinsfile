pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo "Auto Building.. with ${BUILD_ID}"
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
                echo "Auto Deploying.... with ${BUILD_DISPLAY_NAME}"
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
