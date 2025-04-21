pipeline {
    agent any 
    stages {
        stage('checkout SCM') { 
            steps {
                checkout scmGit(branches: [[name: '*/main']],
                 extensions: [], 
                 userRemoteConfigs: [[credentialsId: 'aws_pem',
                 url: 'https://github.com/Suvidha25/Jenkins_new.git']])
            }
        }
        stage('Build') { 
            steps {
                echo "This is for testing" 
            }
        }

    }
}