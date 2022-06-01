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
                sh 'cd googletest/quickstart && make build'
            }
        }
    }
}
