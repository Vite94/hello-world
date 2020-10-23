pipeline {
    agent any
    stages{
        stage('build') {
            steps {
                script{
                    returnedVal = sh (script: 'python script.py', returnStatus: true)
                    if (returnedVal == 1) {
                        withCredentials([usernamePassword(credentialsId: 'github', passwordVariable: 'pass', usernameVariable: 'user')]){
                            echo "$user";   
                        }
                        echo "$returnedVal";    
                    }
                }
            }
        }
    }
}
