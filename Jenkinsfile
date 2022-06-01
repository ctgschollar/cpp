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
                sh '''cd googletest/quickstart
                      ls .
                      make build'''
            }
        }
    }
}
