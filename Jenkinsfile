pipeline {
    agent { label 'test' }
    stages {
        stage('Normal') {
            steps {
                sh 'echo "stage one"'
            }
        }

        stage('parallel') {
            parallel {
                stage('one') {
                    steps {
                        sh 'echo "one"'
                    }
                }
                stage('two') {
                    steps {
                        sh 'echo "two"'
                    }
                }
            }
        }
    }
}
