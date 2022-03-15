pipeline {
    agent any
    tools {
        maven 'Maven'
    }
    stages{
        stage ('Initialize') {
            steps {
                sh '''
                M2_HOME=/opt/maven
                M2=/opt/maven/bin
                PATH=$PATH:$HOME/bin/:$JAVA_home:M2:M2_HOME
                export PATH
                echo "PATH = ${PATH}"
                echo "M2_HOME = ${M2_HOME}"
                whoami
                '''
            }
        }
        // stage ('git cloning'){
        //     step{
        //         git branch: 'main', url: 'https://github.com/SidduChintu/web-application.git'
        //     }
        // }
        // stage ('build'){
        //     step{
        //         build 'pipeline'
        //     }
        // }
        stage ('Build app') {
            steps{
                sh 'mvn clean install package'
            }
        }
    }
}
