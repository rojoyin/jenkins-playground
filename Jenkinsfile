pipeline {
    agent {label 'test'}
    stages {
        stage('prepare-ducttape') {
            steps {
                sh 'echo "prepare-ducttape"'
            }
        }

        stage('frontend') {
            parallel {
                stage('test-coverage') {
                    steps {
                        sh 'echo "test-coverage"'
                    }
                }

                stage('storybook') {
                    steps {
                        sh 'echo "storybook"'
                    }
                }

                stage('check-code') {
                    steps {
                        sh 'echo "check-code"'
                    }
                }

            }
        }

    }
}