pipeline {
    agent none
    stages {
        stage('build') {
            agent {
              docker {
                image 'cpp:base'
                args '-v ${PWD}/googletest/quickstart:/app -w /app'
              }
            }
            steps {
              sh '''
                    ls .
                    make build'''
            }
        }
    }
}
