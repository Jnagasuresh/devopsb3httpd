pipeline {
    agent any
    stages {
        stage ('Build') {
            steps {
                echo "Building the dev"
            }
        }
        stage ('ParallelStageScans') {
            parallel {
                stage ('Sonar') {
                        steps {
                            echo "Sonar Stage Executing"
                            sleep 10
                        }
                    }
                stage ('Fortify') {
                        steps {
                            echo "Sonar Fortiy Executing"
                            sleep 10
                        }
                    }
                    stage ('Prisma') {
                        steps {
                            echo "Sonar Prisma Executing"
                            sleep 10
                        }
                    }
            }
        }
    }
}
