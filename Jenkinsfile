pipeline {
    agent {
        label 'docker-slave'
    }
    environment {
        DOCKER_CREDS = 'dockerhub_creds'
        
    }
    stages {
        stage('build') {
            steps {
                sh "docker pull nginx"
                echo "pulling the image from docker hub"
                sh "docker images"
                sh "docker tag nginx nagasaivardhan/ngnix:sai"
                echo "docker login creditinals"
                sh "docker login -u ${DOCKER_CREDS} -p ${DOCKER_CREDS}"
                sh "docker push nagasaivardhan/ngnix:sai"

            }
        }
    }
}
