pipeline {
    agent {
        label 'AGENT-1'
    }
    // build 
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
    post { 
        always { 
            echo 'I will always say Hello again!'
        } 
        success { 
            echo 'Hello Success' 
        }
        Failure { 
            echo 'Hello failure' 
        }
        
    }
}