pipeline {
    agent any;
    
    tools {
        nodejs "22292-nodejs-tool"
    }
    
    stages {
    
        stage('Initialize') {
            steps {
                sh '''
                    npm install
                '''
            }
        }
        
        stage('Unit Tests') {
            steps {
                sh '''
                    npm run test watchAll=false
                '''
            }
        }
        
        stage('Build') {
            steps {
                sh '''
                    npm run build
                '''
            }
        }
    }
}