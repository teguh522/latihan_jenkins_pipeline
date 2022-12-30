def remote = [:]
remote.name = 'sysadmin'
remote.host = '36.91.115.125'
remote.user = 'sysadmin'
remote.password = 'hasnarsjhmc'
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
