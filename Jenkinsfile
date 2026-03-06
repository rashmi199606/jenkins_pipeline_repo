pipeline {
    agent any   
    stages {
        stage('CEHCKOUT_REPOA') {
            steps {
                checkout ([ $class: 'GitSCM',
                            branches: [[name: '*/main']], 
                            extensions: [], 
                            userRemoteConfigs: [[
                                credentialsId: 'new', 
                                url: 'https://github.com/rashmi199606/rashmisecondrepo.git'
                            ]]
                        ])
               
                sh '''
                    echo 'This is checkout code repo'
                '''
            }
        }

        stage('STAGE1') {
            steps {
                echo "This is stage1 running"
                sh ''' 
                    pwd
                    ls -lrt
                    sleep 5
                '''
            }
        }
    }
}