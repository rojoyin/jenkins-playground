pipeline {
    agent { label 'test' }

    stages {
        stage('prepare-ducttape') {
            steps {
                sh 'echo "prepare-ducttape"'
            }

            stage('frontend') {
                parallel {
                    stage('install-dependencies') {
                        steps {
                            sh 'echo "install-dependencies"'
                        }
                    }

                    parallel {
                        stage('tests-coverage') {
                            steps {
                                sh 'echo "tests-coverage"'
                            }
                        }

                        stage('build-production-storybook') {
                            steps {
                                sh 'echo "build-production-storybook"'
                            }
                        }

                        stage('code-processing') {
                            stages {
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
    }
}