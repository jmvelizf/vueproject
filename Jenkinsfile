pipeline {
    agent {
            docker { 
                image 'node:14-alpine'
                args '-v /var/jenkins_home/build:/dist'
            }
    }
    stages {
            stage('build') {
                steps {          
                    echo 'building the application'
                    sh 'npm install && npm run build'        
                }
            }
    }
        agent none {
            stages {
                    state('deploy') {
            echo 'deploying the application'
                            sh 'docker cp dist static_files:/app/public'
                    }
            
            }
        }
}
