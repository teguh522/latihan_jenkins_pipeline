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
                script{
                    for(int i=8;i<10;i++){
                        echo("script ${i}")
                    }
                }
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
