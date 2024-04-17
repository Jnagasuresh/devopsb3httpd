// based on the branch condition, I can create the pipeline
// BRANCH_NAME variable is only available in Multi Branch pipeline/Git hub or pipelines

pipeline {
    agent any
    environment {
        DEPLOY_TO = "production"
    }
    stages {
        stage ('DeploytoDev')
        {
            steps {
                echo "Deploy to Dev environment"
            }
        }
        stage ('ProdDeploy')
        {
            when {
                // Branch condition
                expression {BRANCH_NAME == /(production|staging)/ }
            }
            steps {
                echo "Production deployments"
            }
        }
    }
}
