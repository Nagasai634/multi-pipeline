pipeline {
    agent any 
    stages {
        stage('build') {
            steps {
                echo "building the code"
            }
        }
        stage('codequality') {
            steps {
                 echo "checking the code quality"
            }
        }
        stage('Dockerbuildnpush') {
            steps {
                echo "building the docker"    
            }
        }
        stage('k8s') {
            steps {
                echo "deploying the image into k8s"
            }
        }
        stage("deploytostage") {
            when {
                branch 'release/*'
            }
            steps {
                echo "deploying the product"
            }
        }
        stage("deploytorelease") {
            when {
               tag pattern: 'v1.2.4.5',comparator: "REGEXP"
            }
            steps {
                echo "deploying the release as tag"
            }
        }
    }
}
