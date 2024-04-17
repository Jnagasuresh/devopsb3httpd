pipeline {
    agent any
    stages {
        stage ('Build') {
            steps {
                echo "building the app"
            }
        }
         stage ('Testing') {
            steps {
                echo "Testing the app"
            }
        }
         stage ('DeployToDev') {
            steps {
                echo "Deploying to Dev Env"
            }
        }
         stage ('DeployToProd') {
            steps {
                timeout (time: 300, unit: 'SECONDS') {
                    input message: 'Would you like to Promote to Prod ??', ok: 'yes', submitter: 'maha'
                }
                echo "Deploying to prod app"
            }
        }
    }
}
