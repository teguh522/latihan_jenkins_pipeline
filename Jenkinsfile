pipeline{
    agent any
    stages{
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