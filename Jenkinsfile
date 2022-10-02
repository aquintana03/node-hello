pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh "npm install"
                sh "sudo mkdir /tp_jenkins"
                sh "sudo git clone https://github.com/aquintana03/node-hello"
                sh "tar czf node_build_$BUILD_NUMBER.tar.gz .git Jenkinsfile index.js package-lock.json package.json"
            }
        }
        stage('test') {
            steps {
                sh "test -f /usr/bin/npm"
                sh "test -f /tp_jenkins/node_build_$BUILD_NUMBER.tar.gz"
            }
        }
        stage('deploy') {
            steps {
                sh "node /tp_jenkins/index.js &"
            }
        }
    }
}
