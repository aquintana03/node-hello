pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh "sudo rm -fr /var/lib/jenkins/workspace/node_test"
                sh "npm install"
                sh "sudo tar czf node_jenkins_$BUILD_NUMBER.tar.gz .git/ Jenkinsfile index.js package-lock.json package.json"
            }
        }
        stage('test') {
            steps {
                sh "test -f /usr/bin/npm"
                sh "test -f /var/lib/jenkins/workspace/node_test/node_jenkins_$BUILD_NUMBER.tar.gz"
            }
        }
     }
}
