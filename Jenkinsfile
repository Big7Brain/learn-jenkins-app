pipeline {
    agent any

    stages {
        stage("without docker"){
            steps{
                echo "hello world"
            }
        }
        stage('with docker') {
            agent{
                docker{
                   image "node:18-alpine" 
                }
                
            }
            steps {
                echo 'Hello World'
                sh "npm --version"
            }
        }
    }
}