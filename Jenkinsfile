pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building.'
            }
        }
        stage('Test') {
            parallel {
                stage('Unit Tests') {
                    steps {
                        sh 'sleep 5s'
                        sh 'echo "Running unit tests"'
                    }
                }
                stage('Integration Tests') {
                    steps {
                        sh 'echo "Running integration tests"'
                    }
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying.'
            }
        }
    }
}
