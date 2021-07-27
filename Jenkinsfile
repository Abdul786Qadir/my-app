pipeline {
    agent any
    stages {
        stage("clone repo") {
            steps {
                sh "rm -rf my-app"
                sh "git clone https://github.com/Abdul786Qadir/my-app.git"
                sh "mvn clean -f my-app"
            }
        }
        stage('Test') {
            steps {
                sh "mvn test -f my-app"
            }
        }
        stage('Deploy') {
            steps {
                sh "mvn package -f my-app"
            }
        }
         post
    {
        always
        {
            emailext body: 'Hi use for pipeline status.', subject: 'pipeline status', to: 'aq2072417@gmail.com'
        }
    }


    }
}

