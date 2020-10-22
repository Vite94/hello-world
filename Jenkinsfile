pipeline {
    agent {
        docker { image 'python:rc-alpine3.12' }
    }
    stage('build') {
        steps {
            sh 'python script.py'
        }
    }
}
