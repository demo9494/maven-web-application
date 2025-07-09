pipeline {
    agent { label 'slave1' }

    stages {
        stage('Bring the code from git') {
            steps {
                git credentialsId: 'git', url: 'https://github.com/demo9494/maven-web-application.git'
            }
        }
    }
}
