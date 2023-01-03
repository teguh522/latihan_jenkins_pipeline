def remote = [:]
remote.name = 'grantia'
remote.host = '36.95.46.181'
remote.user = 'grantia'
remote.password = 'grantiahasna'
remote.allowAnyHosts = true
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
        stage('SSH Remote'){
            steps{
                sshCommand remote: remote, command: "cd fullmmsimrs && git pull origin main"
                sshCommand remote: remote, command: "cd fullmmsimrs && yarn"
            }
        }
    }
    post {
        always {
            echo 'selalu di jalankan'
        }
    }
}
