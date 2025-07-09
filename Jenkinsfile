pipeline {
    agent { label 'slave1' }
    tools{
        maven 'maven-1'
    }

    stages {
        stage('Bring the code from git') {
            steps {
                git credentialsId: 'git', url: 'https://github.com/demo9494/maven-web-application.git'
            }
        }
        stage('Package the code') {
            steps {
                sh 'mvn clean package'
            }
        }
    }
}

