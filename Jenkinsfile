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
                  environment name: 'DEPLOY_TO',value: 'productions'
                }

            }
            steps {
                echo "bulding the next env"
            }
        }
    }
}
