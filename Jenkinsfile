pipeline {
    agent {
       docker { image 'node:14-alpine' }
    }
    stages {
        stage('build') {
            steps {
                echo 'building the application'
								sh 'node --version'
								sh 'ls'
								sh 'npm install && npm run build'        
            }
        }
        stage('test'){
            steps {
                echo 'testing the application'
								sh 'ls'
            }
        }
        stage('deploy') {
            steps {
                echo 'deploying the application'
            }
        }
    }
}
