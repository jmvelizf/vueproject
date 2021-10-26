pipeline {
    agent {
       docker { image 'node:14-alpine', args '-v /var/jenkins_home/build:/dist'}
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
            }
        }
    }
}
