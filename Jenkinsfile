pipeline{
    agent any
    stages{
        stage("create-javaclass"){
            steps{
                bat 'javac Demo1.java'
            }
        }
        stage("run-javaclass"){
            steps{
                bat 'java Demo1'
            }
        }
        stage('Build') {
                    steps {
                        echo 'Building..'
                    }
                }
                stage('Test') {
                    steps {
                        echo 'Testing..'
                    }
                }
                stage('Deploy') {
                    steps {
                        echo 'Deploying....'
                    }
                }
    }
}