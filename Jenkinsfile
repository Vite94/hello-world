pipeline {
    agent any
    stages{
        stage('build') {
            steps {
                script{
                    returnedVal = sh (script: 'python script.py', returnStatus: true)
                    if (returnedVal == 1) {
                        withCredentials([usernamePassword(credentialsId: 'github', passwordVariable: 'pass', usernameVariable: 'user'), usernamePassword(credentialsId: 'rando', passwordVariable: 'pass2', usernameVariable: 'user2')]){
                            if (user == "vite94" && user2 == "rando") {
                                echo "$user";
                                echo "$user2";
                            }
                        }
                        echo "$returnedVal";    
                    }
                }
            }
        }
    }
}
