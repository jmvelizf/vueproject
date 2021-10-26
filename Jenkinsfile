pipeline {
    agent {
       docker { image 'node:14-alpine' }
    }
    stages {
        stage('build') {
            steps {
                echo 'building the application'
								sh 'npm install && npm run build'        
            }
        }
        stage('deploy') {
            steps {
                echo 'deploying the application'
								sh 'docker cp dist static_files:/app/public'
            }
        }
    }
}
