pipeline {
    agent any
    environment {
        DEPLOY_TO = 'production'
    }
    stages {
        stage('build') {
            when {
                allOf {
                                    branch 'production'
                  environment name: 'DEPLOY_TO',value: 'production'
                }

            }
            steps {
                echo "bulding the next env"
            }
        }
    }
}
