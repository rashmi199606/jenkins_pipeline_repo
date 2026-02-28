pipeline {
    agent none
    stages {
        stage('STAGE1') {
            agent { label 'slave1'}
            steps {
                sh 'sleep 5'
                echo "this is stage1"
            }
        }
        stage('Build') {
            agent { label 'slave2'}
            steps {
                sh '''
                   #!/bin/bash
                   pwd
                   ls -lrt
                   sleep 5
                   echo "this is stage2"
                '''   
            }
        }
    }
}