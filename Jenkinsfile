pipeline {
    agent none
    stages {
        stage('build') {
            agent {
                docker { image 'node:14-alpine' }
            }
            steps {
                echo 'building the application'
                sh 'npm install && npm run build' 
            }
        }
        stage('deploy') {
            agent any
            steps {
                echo 'deploying the application'
                sh 'docker cp dist/. static_files:/app/public'
            }
        }
    }
}