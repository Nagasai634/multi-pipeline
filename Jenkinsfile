pipeline {
    agent any
    environment {
        DEPLOY_TO = 'production'
    }
    stages {
        stage('build') {
            when {
                anyOf {
                                    branch 'production'
                  environment name: 'DEPLOY_TO',value: 'productionenv'
                }

            }
            steps {
                echo "bulding the next env"
            }
        }
    }
}
