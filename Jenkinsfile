
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
        stage("deploytoprod") {
            when {
                branch 'production'
            }
            steps {
                echo "deploying the product"
            }
        }
        stage("deploytorelease") {
            when {
                tagname: 'v1.2.4.5'
            }
            steps {
                echo "deploying the release as tag"
            }
        }
    }
}
