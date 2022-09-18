pipeline {
    agent {label 'test'}
    stages {
        stage('Build') {
            steps {
                sh 'echo "building your code"'
            }
        }
        stage('Test') {
            steps {
                sh 'echo "testing your code"'
            }
        }
        stage('Deploy') {
            stages {
                stage('Approval') {
                    steps {
                        sh 'echo "approve deployment"'
                    }
                }
                stage('Deployment') {
                    steps {
                        sh 'echo "deploying your code"'
                    }
                }
            }
        }
    }
}