#!groovy

pipeline {
    agent any
    
    stages {
        stage("checkout code") {
            steps {
                git clone https://github.com/viswa1122/Java_Jenkins_project.git
    }

    stages {
        stage("Build") {
            steps {
                sh "mvn -version"
                sh "mvn clean install"
            }
        }
    }

    post {
        always {
            cleanWs()
        }
    }
}
