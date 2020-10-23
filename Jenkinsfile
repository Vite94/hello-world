pipeline {
    agent any
    stages{
        stage('build') {
            steps {
                script{
                    returnedVal = sh (script: 'python script.py', returnStatus: true)
                    if (returnedVal == 1) {
                        echo "$returnedVal";    
                    }
                }
            }
        }
    }
}
