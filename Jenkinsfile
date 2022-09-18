pipeline {
    agent { label 'test' }
    stages {
        stage('prepare-ducttape') {
            steps {
                sh 'echo "prepare-ducttape"'
            }
        }

        stage('processor') {
            parallel {
                parallel {
                    stage('frontend') {
                        stages {
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
                    stage('backend') {
                        stages {
                            stage('three') {
                                steps {
                                    sh 'echo "three"'
                                }

                            stage('four') {
                                steps {
                                    sh 'echo "four"'
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
