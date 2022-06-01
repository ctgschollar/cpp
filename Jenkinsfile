pipeline {
    agent none
    stages {
        stage('build') {
            agent {
              docker {
                image 'cpp:base'
              }
            }
            steps {
                sh 'echo "YOLO"'
                sh 'ls .'
                sh '''cd googletest/quickstart
                      ls .
                      make build'''
            }
        }
    }
}
