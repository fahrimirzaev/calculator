pipeline {
    agent {
        label 'generic' 
    }
    stages {
        stage("Setup scripts") {
            steps {
                sh """
                    pip install pytest
                """   

            }
        }
        stage("Run unit test"){
            steps {
                sh """
                    python -m pytest
                """
            }
        }
    }
    post {
        always {
            sh """
                pip uninstall pytest -y
            """
        }
    }
}
