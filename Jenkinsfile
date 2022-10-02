pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh "sudo rm -fr /tp_node_jenkins"
                sh "npm install"
                sh "sudo mkdir /tp_node_jenkins"
                sh "sudo git clone https://github.com/aquintana03/node-hello /tp_node_jenkins"
                sh "sudo tar czf node_jenkins.tar.gz .git/ Jenkinsfile index.js package-lock.json package.json"
            }
        }
        stage('test') {
            steps {
                sh "test -f /usr/bin/npm"
                sh "test -f /tp_node_jenkins/node_jenkins.tar.gz"
            }
        }
        stage('deploy') {
            steps {
                sh "node /tp_jenkins/index.js &"

            }
        }
    }
