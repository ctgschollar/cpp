pipeline {
    agent none
    stages {
        stage('build') {
            agent {
              docker {
                image 'cpp:base'
                args '-v ${PWD}:/app'
              }
            }
            steps {
                sh 'echo "YOLO"'
                sh 'ls .'
            }
        }
    }
}
