def remote = [:]
remote.name = 'sysadmin'
remote.host = '192.168.50.3'
remote.user = 'sysadmin'
remote.password = 'hasnarsjhmk'
remote.allowAnyHosts = true

pipeline {
    agent any
    stages {
            stage('Remote SSH') {
                steps {
                sshCommand remote: remote, command: 'ls -l'
                }
            }
        stage('hello') {
            steps {
                echo 'hello'
            }
        }
    }
    post {
        always {
            echo 'selalu di jalankan'
        }
    }
}
