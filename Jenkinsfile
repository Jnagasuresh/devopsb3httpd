pipeline {
    agent any
    environment {
        DEPLOY_TO = 'production'
    }
    stages {
        stage ('ProdDeploy'){
            when {
                environment name: 'DEPLOY_TO', value: 'other'
            }
            steps {
                echo "Deployin to production"
            }
        }
    }
}
