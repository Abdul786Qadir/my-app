pipeline {
    agent any
    stages {
        stage("clone") {
            steps {
                
                sh "rm -rf my-app"
                sh "git clone https://github.com/Abdul786Qadir/my-app.git"
                sh "mvn clean -f my-app"    
            }
        }
        stage('Test maven project') {
            steps {
                
                sh "mvn test -f my-app"
            }
        }
        stage('Deploy') {
            steps {
                sh "mvn package -f my-app"
            }
        }
       
    }
}

