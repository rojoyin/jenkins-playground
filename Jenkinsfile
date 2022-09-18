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
                    stages{
                        stage('validate-code-changes') {
                            steps {
                                sh 'echo "validate-code-changes"'
                            }
                        }

                        stage('build-prod-app') {
                            steps {
                                sh 'echo "build-prod-app"'
                            }
                        }

                        stage('publish') {
                            steps {
                                sh 'echo "publish"'
                            }
                        }
                    }
                }

            }
        }

    }
}