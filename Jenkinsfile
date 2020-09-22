pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Hello World ...'
            }
        }
        stage('Testing') {
            steps {
                echo 'Testing ...'
            }
        }
        stage('Deploy master') {
            steps {
                when {
                    branch 'master'
                }
                script {
                    echo 'I only execute on the master branch'    
                }
            }
        }
        stage('Deploy staging') {
            steps {
                when {
                    branch 'staging'
                }
                script {
                    echo 'I only execute on the staging branch'    
                }
            }
        }
    }
    post {
        always {
            echo 'This will always run'
        }
        success {
            echo 'This will run only if successful'
        }
        failure {
            echo 'This will run only if failed'
        }
    }
}