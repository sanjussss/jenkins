pipeline {
    agent none 
    stages {
        stage('Build') {
            agent any
            steps {
          
                sh '''
                    #!/bin/bash 
                    pwd 
                    ls
                    echo "This is a BUILD stage"
                    sleep 5
                '''  
            }
        }

        stage('DEPLOY') {
            agent { label 'slave' } 
            steps {
                echo "This is a DEPLOY stage"
                sh 'sleep 5'
            }
        }

        stage('TESTING1') {
            agent { label 'slave' } 
            steps {
                sh 'echo "This is a TESTING1 stage"'
                sh 'sleep 5'
            }
        }

        stage('TESTING2') {
            agent { label 'slave'}
            steps {
                sh '''
                    echo "This is a TESTING2 stage"
                    sleep 5
                '''
            }
        }
    }
}
