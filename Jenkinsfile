pipeline {
    agent any

    triggers {
        githubPush()
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/hansikagollen/python-project.git'
            }
        }

        stage('Run Python Script') {
            steps {
                bat 'python app.py'
            }
        }
    }

    post {
        always {
            echo 'Build finished. Check console output for Python result.'
        }
    }
}
