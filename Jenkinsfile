pipeline {
    agent any

    parameters {
        string(name: 'APP_NAME', defaultValue: 'Jenkins Demo', description: 'Application Name')

        choice(name: 'ENVIRONMENT',
               choices: ['Development', 'Testing', 'Production'],
               description: 'Select Environment')

        booleanParam(name: 'RUN_TESTS',
                     defaultValue: true,
                     description: 'Run Tests?')
    }

    stages {

        stage('Build') {
            steps {
                echo "Building ${params.APP_NAME}"
            }
        }

        stage('Run Tests') {

            when {
                expression {
                    return params.RUN_TESTS
                }
            }

            steps {
                echo "Running Tests..."
                bat 'echo All Tests Passed'
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying to ${params.ENVIRONMENT}"
            }
        }
    }
}