
pipeline {
    agent any 
    environment {
        DEPLOY_TO ='production'
    }
    stages {
        stage('proddeploy') {
            when {
               environment name: 'DEPLOY_TO', value: 'productions' 
            }
            steps {
                echo "building the production"
            }
        }
    }
}
