def remote = [:]
remote.name = 'grantia'
remote.host = '36.95.46.181'
remote.user = 'grantia'
remote.password = 'grantiahasna'
remote.allowAnyHosts = true
pipeline {
    agent any
    stages {
        stage('Git') {
            steps {
                withCredentials([usernamePassword(credentialsId: 'teguh522-github')]) {
                sh """
                git checkout dev
                git log --oneline
                """
                }
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
