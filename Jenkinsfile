pipeline {
    agent any

    stages {

        stage('Display Workspace') {
            steps {
                bat 'echo Workspace: %WORKSPACE%'
            }
        }

        stage('List Files') {
            steps {
                bat 'dir'
            }
        }

        stage('Read File') {
            steps {
                bat 'type hello.txt'
            }
        }

        stage('Run Script') {
            steps {
                bat 'hello.bat'
            }
        }

        stage('Finish') {
            steps {
                bat 'echo Pipeline Completed Successfully!'
            }
        }

    }
}