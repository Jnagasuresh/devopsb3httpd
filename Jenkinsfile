pipeline {
    agent any
    environment {
        DEPLOY_TO ='production'
    }
    stages {
        stage ("DeploytoDev") {
            steps {
                echo 'Deploying to Dev Environment'
            }
        }
        stage ("ProductionDeploy") {
            when {
                allOf {
                    branch 'production'
                    environment name: 'DEPLOY_TO', value: 'production'
                }
            }
            steps {
                echo 'Deploying to production Environment'
            }
        }
    }
}
