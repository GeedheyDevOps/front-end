pipeline {
    agent any
    tools {
        nodejs 'NodeJS 11.0.0' 
        docker 'docker'
    }
    stages {
        stage('Build') {
            tools {
                nodejs 'NodeJS 4.8.6'
            }
            steps {
                echo "Building Stage...."
                sh 'npm install'
            }
        }
        
        stage('Test') {
            steps {
                echo "Testing Stage...."
                sh 'npm install'
                sh 'npm run test'
                sh 'npm run coverage'
            }
        }
        
        stage('Package') {
            steps {
                echo "Packaging Stage...."
                sh 'npm install'
                sh 'npm run package'
            }
        }
    }
}
