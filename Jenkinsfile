pipeline {
    agent { docker 'python:3.10-rc' }
    stages {
        stage('build') {
            steps {
                sh 'python script.py'
            }
        }
    }
}
