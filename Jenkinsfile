pipeline {
    agent { label 'test' }
    stages {
        stage('Normal') {
            steps {
                sh 'echo "stage one"'
            }
        }

        stage('frontend') {

            parallel{

        

        stage('parallel1') {
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

        stage('parallel2') {
            steps {
                sh 'echo "parallel2"'
            }
        }

        }}
    }
}
