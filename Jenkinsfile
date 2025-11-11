pipeline{
     agent any
     environment{
        PYTHON = 'C:\\Program Files\\Python314\\python.exe
'
     }
     stages{
        stage('checkout code') {
            steps
            {
           checkout scm
           }
        }
        stage('extract data') {
            steps{
            bat "${env.PYTHON} extract_data.py"
            }
        }
     }
     post 
     success{
           echo "success...."
     }
     failure{
            echo "fail..."
     }
     always{
            echo "always..."
     }
}