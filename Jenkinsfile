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

    tools {
        Maven "3.6.0" // You need to add a maven with name "3.6.0" in the Global Tools Configuration page
    }

    stages {
        stage("Build") {
            steps {
                sh "mvn -version"
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
