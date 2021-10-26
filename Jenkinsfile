pipeline {
    agent {
       docker { image 'node:14-alpine' }
    }
    stages {
        stage('build') {
            steps {
                echo 'building the application'
								sh 'npm run build'        
            }
        }
        stage('test'){
            steps {
                echo 'testing the application'
            }
        }
        stage('deploy') {
            steps {
                echo 'deploying the application'
            }
        }
    }
}
