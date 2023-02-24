pipeline {
    agent any

    environment {
        PATH = "/usr/local/bin:${PATH}"
    }

    stages {

        stage('Install Dependencies') {
            steps {
                sh 'pip install -r requirements.txt'
            }
        }

        stage('Build') {
            steps {
                sh 'python gpt2.py build'
            }
        }
        stage('Cleanup') {
            steps {
                sh 'rm -rf build dist'
            }
        }
    }
}