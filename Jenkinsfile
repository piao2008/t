pipeline{
    agent any
    stages{
        stage("pull start"){
           steps{
            echo 'start..'
           }
        }

        stage("build pacakge"){
            steps{
            echo 'build start...'
            }
        }

        stage('deploy'){
            steps{
                echo 'deploy start...'
            }
        }

    }
    post{
    always {
        echo 'send email....'
    }
    }
}