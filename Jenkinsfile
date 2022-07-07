#!groovy

pipeline {
    agent any
    
    stages {
        stage("checkout code") {
            steps {
                git 'https://github.com/viswa1122/Java_Jenkins_project.git'
            }
        }       
    }
    stages {
        stage("Build") {
            steps {
                sh "mvn clean install package"
            }
        }
    }
    post {
        always {
            cleanWs()
        }
    }
}
