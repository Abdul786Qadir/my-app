pipeline {
    agent any

    stages
    {
        stage('Build') {
            steps {
                echo 'Build application'
            }
        }pipeline {
    agent any

    stages
    {
        stage('Build') {
            steps {
                echo 'Build application'
            }
        }
         stage('Test') {
            steps {
                echo 'Test application'
            }
        }
         stage('Deploy') {
            steps {
                echo 'Deploy application'
            }
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
