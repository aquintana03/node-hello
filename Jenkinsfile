pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh "npm install"
                sh "sudo tar czf node_jenkins.tar.gz .git/ Jenkinsfile index.js package-lock.json package.json"
            }
        }
        stage('test') {
            steps {
                sh "test -f /usr/bin/npm"
                sh "test -f /var/lib/jenkins/workspace/node3/node_jenkins.tar.gz"
            }
        }
        stage('deploy') {
            steps {
                sh "sudo mkdir /node_app"
                sh "sudo tar xzvf node_jenkins.tar.gz /node_app" 
                sh "sudo node /node_app/index.js"
            }
        }
    }
}
