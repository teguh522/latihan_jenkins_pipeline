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
            when{
                branch "dev"
            }
            steps {
                sh '''git checkout main
                git pull origin main
                git cherry-pick ${GIT_COMMIT}
                git add .
                git commit
                git push origin main
                '''
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
