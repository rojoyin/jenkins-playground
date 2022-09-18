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
                        'echo "storybook"'
                    }
                }

                stage('check-code') {
                    steps {
                        'echo "check-code"'
                    }
                }

            }
        }

    }
}