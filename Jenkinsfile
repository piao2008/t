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
    post {
      always {
       emailext body: '''<html>
       <h1>total cases: ${TEST COUNTS,var="total"}</h1>
       <h1>pass cases: ${TEST COUNTS,var="pass"}</h1>
       <h1>fail cases:${TEST COUNTS,var="fail"}</h1>
       <html>''', subject: 'pipeline-demo-测试', to: '6411111@qq.com'
      }
publishHTML([allowMissing: true, alwaysLinkToLastBuild: true, keepAll: true, reportDir: 'report', reportFiles: 'index.html', reportName: 'HTML Report', reportTitles: '', useWrapperFileDirectly: true])
    }
}