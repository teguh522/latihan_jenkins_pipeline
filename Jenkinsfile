pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo "Hallo build"
            }
        }
        stage('Test') {
            steps {
                echo 'Hello test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Hello deploy'
            }
        }
    }
    post {
        always {
            echo 'selalu di jalankan'
        }
    }
}
