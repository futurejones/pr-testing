pipeline {
    agent { label 'swiftaltra' }
    
    environment {
        //
        MESSAGE='Hello World'
   }

    stages {
        stage('Hello') {
            steps {
                cleanWs()
                sh "echo '${MESSAGE}'
                sh "echo '${MESSAGE}' > hello.txt"                
                sh 'tar -cf hello.tar hello.txt'
                sh 'ls'
            }
        }
        stage ('Run Local CMD') {
            steps {
                sh 'apt-get update'
            }
        }
    }
}
