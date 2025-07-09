pipeline{
    agent "slave1"
    stages{
        stage("Bring the code from git"){
            git credentialsId: 'git', url: 'https://github.com/demo9494/maven-web-application.git'
        }
            }//stage ending
}//pipeline ending
