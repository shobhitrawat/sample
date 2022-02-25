pipeline {
    agent any
environment{
    MAVEN_HOME="/usr/local/mvn"
    }

    stages {
        stage('Test') {
            steps {
                sh '''
                echo $JAVA_HOME
                echo $MAVEN_HOME
        
                '''
            }
        }
        
        stage('Build') {
            steps {
                echo 'Hello Build'
                sh '''
                ls
                date
                pwd
                '''
            }
        }
        
        stage('Deploy') {
            environment{
            MVN_HOME="/opt/mvn"
            }
            steps {
               sh '''
               echo $MVN_HOME
               echo $USERNAME
               '''            
                    }
            }
        
    }

 post{
     always{
         echo "Always"
    }
     success{
     echo "Build Success"
                }
     failure{
     echo "Build Failed"
                }
}
     
}

