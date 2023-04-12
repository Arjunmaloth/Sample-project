pipeline {
    agent any
    environment {
        CI = "true"
    }
    tools {
       // nodejs "node"
    }
    stages {
        stage('Build') {
            steps {
                echo 'Build'
            }
        }
        stage('Test') {
            steps {
                echo 'Test'
            }
        }
        stage('Deploy') {
            steps {
                 echo 'Deploy'
            }
        }
    }
    post {
        always{
            echo 'Post stage'
        }
        success{
            mail bcc: '', body: "<b>Project Status - Your project pipeline ran successfully.</b><br>Project: ${env.JOB_NAME} <br>Build Number: ${env.BUILD_NUMBER} <br> URL de build: ${env.BUILD_URL}", cc: '', charset: 'UTF-8', from: 'malotharjun9909@gmail.com', mimeType: 'text/html', replyTo: '', subject: "Success: Project Successfully builded", to: "malotharjun9909@gmail.com";
        }
        failure{
            mail bcc: '', body: "<b>Project Status - Your project pipeline has failed.</b><br>Project: ${env.JOB_NAME} <br>Build Number: ${env.BUILD_NUMBER} <br> URL de build: ${env.BUILD_URL}", cc: '', charset: 'UTF-8', from: 'malotharjun9909@gmail.com', mimeType: 'text/html', replyTo: '', subject: "ERROR: Project pipeline failed", to: "malotharjun9909@gmail.com";
        }
    }
}