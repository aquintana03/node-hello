pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh "npm install"
                sh "sudo mkdir /tp_jenkins"
                sh "sudo git clone https://github.com/aquintana03/node-hello /tp_jenkins"
            }
        }
        stage('test') {
            steps {
                sh "test -f /usr/bin/npm"
                sh "test -f /tp_jenkins/index.js"
            }
        }
        stage('deploy') {
            steps {
                sh "node /tp_jenkins/index.js &"
            }
        }
    }
}
