node {
    def PYTHON = 'C:\\Program Files\\Python314\\python.exe'

    try {
        stage('Checkout') {
            checkout scm
        }

        stage('Extract Data') {
            bat "${PYTHON} extract.py"
        }

    } catch (err) {
        echo "Pipeline failed: ${err}"
        currentBuild.result = 'FAILURE'
    } finally {
        echo 'Pipeline completed.'
    }
}

