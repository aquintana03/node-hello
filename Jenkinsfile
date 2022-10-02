pipeline {
    agent any

    stages {
        stage('build') {
            steps {
                node index.js
            }
        }
        stage('test') {
            steps {
                node -v
            }
        }
    }
}
