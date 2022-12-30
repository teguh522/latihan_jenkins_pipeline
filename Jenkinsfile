pipeline{
    agent {
    node {
    def remote = [:]
    remote.name = 'palimanan'
    remote.host = '192.168.45.3'
    remote.user = 'sysadmin'
    remote.password = 'hasnarsjhmc'
    remote.allowAnyHosts = true
    }
    }

    stages{
            stage('Remote SSH') {
            sshCommand remote: remote, command: "ls -l"
        }
        stage("hello"){
            steps{
                echo "hello"
            }
        }
    }
    post{
        always{
            echo "selalu di jalankan"
        }
    }
}