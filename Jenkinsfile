pipeline {
    agent any
    stages {
        stage('check docker') {
            steps {
                echo 'checking..'
                sh '''
                    docker --version
                    /usr/local/bin/docker-compose --version'''
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Build') {
            steps {
                echo 'Deploying..'
                sh '/usr/local/bin/docker-compose up -d'
            }
        }
    }
}