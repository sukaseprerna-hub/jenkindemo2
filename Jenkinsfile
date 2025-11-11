pipeline {
    agent any

    environment {
        PYTHON = 'C:\\Program Files\\Python314\\python.exe'
    }

    stages {
        stage('Checkout Code') {
            steps {
                checkout scm
            }
        }

        stage('Extract Data') {
            steps {
                bat "\"${env.PYTHON}\" extract.py"
            }
        }
    }

    post {
        success {
            echo "success...."
        }
        failure {
            echo "fail..."
        }
        always {
            echo "always..."
        }
    }
}
