pipeline {
    agent none
    stages {
        stage('build') {
            agent any
            steps {
                sh 'echo "YOLO"'
                sh 'docker build -t cpp:base -f base/Dockerfile .'
            }
            {
                sh 'ls /var/jenkins_home/workspace/cpp@2/googletest/quickstart'
                sh 'docker run --rm -v ${PWD}:/app cpp:base ls .'
                sh 'docker run --rm -v ${PWD}:/app cpp:base ls /app'
                sh '''cd googletest/quickstart
                      echo ${PWD}
                      ls .
                      docker run --rm -v /var/jenkins_home/workspace/cpp@2/googletest/quickstart:/app cpp:base ls .
                      docker run --rm -v /var/jenkins_home/workspace/cpp@2/googletest/quickstart:/app cpp:base ls /app'''
            }
        }
    }
}
