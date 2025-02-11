pipeline{
    agent any
    environment {
            LANG = 'zh_CN.UTF-8'
            LC_ALL = 'zh_CN.UTF-8'

        }
    stages{
        stage("create-javaclass编译java"){
            steps{

                echo $LANG
                echo $LC_ALL
                locale
                //bat 'chcp 65001'
                echo "开始编译java源文件"
                //指定编译时的编码
                bat 'javac -encoding UTF-8 Demo1.java'

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
       <html>''',
        subject: 'pipeline-demo-测试', to: '6411111@qq.com'
      }

    }
}