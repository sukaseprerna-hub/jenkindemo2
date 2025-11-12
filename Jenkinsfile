pipeline {
    agent any

   triggers {
        cron('*/2 * * * *') 
    }
    environment {
        PYTHON = 'C:\Program Files\Python314\python.exe'
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Setup Python') {
            steps {
                bat "${env.PYTHON} --version"
            }
        }

        stage('Extract') {
            steps {
                bat "\"${env.PYTHON}\"extract_data.py extract.py"
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed.'
        }
        failure {
            echo 'Pipeline failed.'
        }
    }
}




