pipeline {
    agent any

    stages {
        stage('Install_Node') {
            steps {
                sh 'npm install' 
            }
        }
        stage('build') {
            steps {
                sudo node index.js
            }
        }
        stage('test') {
            steps {
                sudo node -v
            }
        }
    }
}
