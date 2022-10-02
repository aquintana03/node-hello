pipeline {
    agent any

    stages {
        stage('Install_Node') {
            steps {
                sudo apt install nodejs 
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
