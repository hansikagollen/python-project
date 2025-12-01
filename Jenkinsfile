pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/hansikagollen/python-project.git'
            }
        }

        stage('Run Python Script') {
            steps {

                bat 'python addition.py'
            }
        }
    }

    post {
        always {
            echo 'Build finished. Check console output for Python result.'
        }
    }
}
