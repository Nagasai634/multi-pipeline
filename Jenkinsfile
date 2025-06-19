pipeline {
    agent any

    stages {
        stage('parallel-tasks') {
            parallel {
                stage('build') {
                    steps {
                        echo "building the code"
                        sleep 10
                    }
                }
                stage('codequality') {
                    steps {
                        echo "checking the code quality"
                        sleep 10
                    }
                }
            }
        }

        stage('build') {
            steps {
                echo "welcome to my first pipeline"
            }
        }

        stage('sonar') {
            steps {
                echo "scanning the code"
            }
        }

        stage('docker') {
            steps {
                echo "building the docker image"
            }
        }

        stage('kube') {
            steps {
                echo "deploying to k8s"
            }
        }
    }
}
