pipeline {

    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Repository Checked Out'
            }
        }

        stage('Compile') {
            steps {
                bat 'gcc hello.c -o hello.exe'
            }
        }

        stage('Run') {
            steps {
                bat 'hello.exe'
            }
        }

    }

    post {
        success {
            echo 'Pipeline Executed Successfully'
        }
        failure {
            echo 'Pipeline Failed'
        }
    }

}