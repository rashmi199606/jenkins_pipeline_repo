pipeline {
    agent any
    stage {
        stage('STAGE1') {
            steps{
                sh 'sleep'
                echo "This is jenkis stage1"
            }
        }
        stage('STAGE2') {
            steps{
                sh '''
                #!/bin/bash
                pwd
                ls -lrt
                sleep 5
            }
        }
    }
}