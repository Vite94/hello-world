pipeline {
    agent any
    stages{
        stage('build') {
            steps {
                returnedVal = sh (script: 'python script.py', returnStatus: true)
                echo "$returnedVal"
            }
        }
    }
}
