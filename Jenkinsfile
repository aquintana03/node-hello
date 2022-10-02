pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh "npm install"
            }
        }
        stage('test') {
            steps {
                sh "test -f /usr/bin/npm"
            }
        }
    }
}
