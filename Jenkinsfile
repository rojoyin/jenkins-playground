pipeline {
    agent { label 'test' }
    stages {
        stage('Normal') {
            steps {
                sh 'echo "stage one"'
            }
        }
        stage('Parallel') {
            parallel {
                stage('paraINpara') {
                    steps {
                        sh 'echo "nesting parallel not supported"'
                    }
                }
                stage('seqINpara') {
                    stages {
                        stage('one') {
                            steps {
                                echo "stage one"
                            }
                        }
                        stage('two') {
                            steps {
                                echo "stage one"
                            }
                        }
                    }    
                }
            }
        }
        stage('Sequestial') {
            stages {
                stage('seqINseq') {
                    stages {
                        stage('one') {
                            steps {
                                echo "stage one"
                            }
                        }
                        stage('two') {
                            steps {
                                echo "stage one"
                            }
                        }
                    }  
                }
                stage('paraINseq') {
                    parallel {
                        stage('one') {
                            steps {
                                echo "stage one"
                            }
                        }
                        stage('two') {
                            steps {
                                echo "stage one"
                            }
                        }
                    }
                }
            }
        }
    }
}
