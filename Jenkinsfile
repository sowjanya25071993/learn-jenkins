pipeline {
    agent {
        node {
            label 'Agent-1'
        }
    } //build
    environment {
        GREETING = 'HELLO JENKINS'
    }
    options {
        timeout(time: 1, unit: 'HOURS') 
    }
    stages {
        stage('Build') { 
            steps {
            echo 'building'
            }
        }
        stage('Test') { 
            steps {
                echo 'testing'
            }
        }
        stage('Deploy') { 
            steps {
                sh """
                  echo "here i wrote shell script"
                  echo "$GREETING"
                  sleep 10
                """
            }
        }
    }
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
        failure { 
            echo 'this runs when pipeline is failed... used to send some alerts'
        }
        success { 
            echo 'I will always say Hello when pipeline is success'
        }
    }
}
