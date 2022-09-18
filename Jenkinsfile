pipeline {
    agent {label 'test'}
    stages {
        stage('prepare-ducttape') {
            steps {
                sh 'echo "prepare-ducttape"'
            }
        }

        parallel {
            stage('frontend') {
                stages {
                    stage('install-dependencies') {
                        steps {
                            sh 'echo "install-dependencies"'
                        }
                    }
                }

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

                }
            }

            stage('backend') {
                stages {
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
}