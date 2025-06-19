pipeline {
    agent any
    stages {
        stage('develop') {
            steps {
                echo "welcome to develop stage1"
            }
        }
        stage('production') {
            steps { 
                when {
                    expression {BRANCH_NAME==~ /('production|develop')/}
                }
                echo "welcome to production stage2"
            }
        }
    }
}
