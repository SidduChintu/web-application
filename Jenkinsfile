pipelines {
    agent any
    stages{
        stage ('git cloning'){
            step{
                git branch: 'main', url: 'https://github.com/SidduChintu/web-application.git'
            }
        }
        stage ('build'){
            step{
                build 'pipeline'
            }
        }
    }
}
