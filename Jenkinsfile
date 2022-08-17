pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Auto Building..'
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
                echo 'Auto Deploying....'
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
