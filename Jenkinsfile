pipeline {
    agent { label 'test' }
    stages {
        stage('Normal') {
            steps {
                sh 'echo "stage one"'
            }
        }

        stage('first-fork') {
            parallel {
                stage('one') {
                    step {
                        sh 'echo "one"'
                    }
                }

                stage('two') {
                    step {
                        sh 'echo "two"'
                    }
                }
            }
        }
    }
}
