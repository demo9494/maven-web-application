pipeline {
    agent { label 'slave1' }
    tools{
        maven 'maven1'
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
        stage('Deploy to tomcat') {
            steps {
               sshagent(['tomcat']) {
                sh 'scp *.war ubuntu@13.235.45.237:/opt/apache-tomcat-9.0.107/webapps'
   
            }
        }
    }
}
}
