pipeline {
    agent {
        label 'AGENT-1'
    }
    environment {
        COURSE = 'jenkins'
    }
    options {
        timeout(time: 1, unit: 'SECONDS')
    }
   // Build  
    stages {
        stage('Build') {
            steps { 
                script{
                    sh """
                        echo "hello build" 
                        sleep 10
                        env
                    """
                }
            }
        }
        stage('Test') {
            steps { 
                script{
                    echo 'Testing..'
                }
            }
        }
        stage('Deploy') {
            steps {
                script{
                   echo 'Deploying....'
                }
            }
        }
    } 

    post { 
        always { 
            echo 'I will always say Hello again!'
            deleteDir()
        } 
        success { 
            echo 'Hello Success'
        } 
        failure { 
            echo 'Hello failure'
        }
    }

}


 