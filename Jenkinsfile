pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo "Hallo build"
                sleep(5)
                sh("ls -a")
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
