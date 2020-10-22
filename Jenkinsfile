pipeline {
    agent {
        docker { image 'python:rc-alpine3.12' }
    }
    stages{
        stage('build') {
            steps {
                sh 'python script.py'
            }
        }
    }
}
