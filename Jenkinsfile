pipeline {
    agent none
    stages {
        stage('build') {
            agent any
            steps {
                sh 'echo "Hello World"'
                sh 'echo ${PWD}'
                sh 'ls'
                sh 'docker build -t cpp:base -f base/Dockerfile .'
                sh 'echo "Hello World"'
                sh 'echo ${PWD}'
                sh 'ls'
                sh 'cd googletest/quickstart && make build'
            }
        }
    }
}
