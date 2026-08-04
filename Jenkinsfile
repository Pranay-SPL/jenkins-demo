pipeline {
    agent any

    parameters {
        string(name: 'APP_NAME', defaultValue: 'Jenkins Demo', description: 'Enter Application Name')

        choice(name: 'ENVIRONMENT', choices: ['Development', 'Testing', 'Production'], description: 'Select Environment')

        booleanParam(name: 'RUN_TESTS', defaultValue: true, description: 'Run Tests?')
    }

    stages {

        stage('Display Parameters') {
            steps {
                bat """
                echo ==========================
                echo Application : %APP_NAME%
                echo Environment : %ENVIRONMENT%
                echo Run Tests   : %RUN_TESTS%
                echo ==========================
                """
            }
        }

        stage('Run Batch File') {
            steps {
                bat 'hello.bat'
            }
        }
    }
}