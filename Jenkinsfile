pipeline {
    agent {
        node {
            label 'Agent-1'
        }
    } //build
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
                echo 'deploying'
            }
        }
    }
}
