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
                sshagent(credentials: ['majalengka-ssh']) {
                sh('''
                    ssh -o StrictHostKeyChecking=no grantia@36.95.46.181
                    ls -a
                ''')
                }
            }
        }
    }
    post {
        always {
            echo 'selalu di jalankan'
        }
    }
}
