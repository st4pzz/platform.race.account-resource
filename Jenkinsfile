pipeline {
    agent any
    stages {
        stage('Jenkins Account') {
            steps {
                echo 'Account Service'
            }
        }
        stage('Build Interface') {
            steps {
                build job: 'store.account', wait: true
            }
        }
        stage('Build') { 
            steps {
                sh 'mvn clean package'
            }
        }      
    }
}