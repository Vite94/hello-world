pipeline {
    agent any
    stages{
        stage('build') {
            steps {
                step{
                    returnedVal = sh (
                        script: 'python script.py',
                        returnStatus: true
                        )
                    echo "$returnedVal"
                }
            }
        }
    }
}
