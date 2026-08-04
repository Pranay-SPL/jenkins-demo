pipeline {
    agent any

    stages {

        stage('Display Files') {
            steps {
                bat 'dir'
            }
        }

        stage('Run Batch File') {
            steps {
                bat 'hello.bat'
            }
        }

        stage('Read Text File') {
            steps {
                bat 'type hello.txt'
            }
        }

    }
}