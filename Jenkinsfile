pipeline {
    agent any
    parameters {
        string(name:'NAME', defaultValue:'Nags', description: 'Name of the person')
        text(name:'PARA', defaultValue:'', description: 'Enter highlevel  fixes for the release')
        choice(name:'ENV', choices: ['dev', 'Test', 'Prod'], description: 'Which environment would you like to deploy')
        booleanParam(name:'TOOGLEAME', defaultValue:true, description: 'Would you like to scan')
        password(name:'SECRET', defaultValue:'SECUREPASSWORD', description: 'Enter the password')
    }
    stages {
        stage ('ParametersExample') {
            steps {
                echo "Welcom ${params.NAME}"
                echo "Fixes done are  ${params.PARA}"
                echo "Deploying to  ${params.ENV}"
                echo "The Password entered is ${params.SECRET}"
            }
        }

    }
}
