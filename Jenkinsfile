pipeline {
    agent any
    
    parameters {
        choice(name: 'VERSION', choices:['1.1.0','1.2.0'.'1.3.0'], description:'')
        booleanParam(name: 'executeTests', defaultValue: true, description:'')
    }

    stages {
        stage('Build') {
            steps {
                echo "Auto Building with ${BUILD_ID}"
            }
        }
        stage('Test') {
            when { 
                expression {
                    BRANCH_NAME == 'main' && params.executeTests == true
                }
            }
            steps {
                echo 'Auto Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo "Auto Deploying.... with ${BUILD_DISPLAY_NAME} and ${params.VERSION}"
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
