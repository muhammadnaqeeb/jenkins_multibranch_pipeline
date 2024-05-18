pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    if (isUnix()) {
                        sh '''
                        echo "Building App..."
                        node --version
                        '''
                    } else {
                        bat '''
                        echo Building App...
                        node --version
                        '''
                    }
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    if (isUnix()) {
                        sh '''
                        echo "Testing App..."
                        node main.js
                        '''
                    } else {
                        bat '''
                        echo Testing App...
                        node main.js
                        '''
                    }
                }
            }
        }
    }
}
