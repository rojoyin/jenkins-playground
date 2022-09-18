pipeline {
    agent { label 'test' }
    stages {
        stage('prepare-ducttape') {
            steps {
                sh 'echo "prepare-ducttape"'
            }
        }

        stage('process') {
            parallel {
                stage('frontend') {
                    stages {
                        stage('one') {
                            steps {
                                sh 'echo "one"'
                            }
                        }
                    }

                    stages {
                        stage('two') {
                            steps {
                                sh 'echo "two"'
                            }
                        }
                    }
                    
                }
            }
        }
    }
}
