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
        stage('Deploy') {
            when{
                branch 'master'
            }
            steps {
                echo 'run this stage - ony if the branch = master branch'
            }
            when{
                branch 'staging'
            }
            steps {
                echo 'run this stage - ony if the branch = staging branch'
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