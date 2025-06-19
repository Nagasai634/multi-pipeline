pipeline {
    agent {
        label:'docker-slave'
    }
    stages {
        stage('build') {
            steps {
                sh "docker pull nginx "
                echo "pulling the image from docker hub"
                sh "docker images"
            }
        }
    }
}
