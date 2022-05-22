pipeline {
    agent none
    stages {
        stage('build') {
            agent any
            steps {
                sh 'docker build -t cpp:base -f base/Dockerfile .'
            }
            {
                sh 'cd googletest/quickstart && make build'
            }
        }
    }
}
