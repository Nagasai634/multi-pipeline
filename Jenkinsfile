
pipeline {
    agent any
    stages {
        stage('develop') {
            steps {
                echo "welcome to develop stage1"
            }
        }
        stage('production') {
            when {
                    expression {BRANCH_NAME==~ /('production|develops')/}
                }
            steps { 
                echo "welcome to production stage2"
            }
        }
    }
}
