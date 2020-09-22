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
        stage('Deliver for development') {
            when {
                branch 'development' 
            }
            steps {
                echo 'development'
            }
        }
        stage('Deploy for production') {
            when {
                branch 'master'  
            }
            steps {
                echo 'master'
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