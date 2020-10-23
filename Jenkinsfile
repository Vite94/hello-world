pipeline {
    agent any
    stages{
        stage('build') {
            steps {
                script{
                    returnedVal = sh (script: 'python script.py', returnStatus: true)
                    if (returnedVal == 1) {
                        withCredentials([usernamePassword(credentialsId: 'github', passwordVariable: 'pass', usernameVariable: 'user')]){
                            if (user == "vite94") {
                                echo "$user";
                            }
                        }
                        echo "$returnedVal";    
                    }
                }
            }
        }
    }
}
