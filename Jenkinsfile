pipeline{
    agent any
    
    stages{
        stage('clone'){
            steps{
                git 'https://github.com/chetanbkcbk/publicrepo.git'
            }
        }
        stage('build'){
            steps{
                sh 'docker build -t weapp /var/lib/jenkins/workspace/docker/.'
            }
        }
        stage('run'){
            steps{
                sh 'docker run -d -it --name cont_weapp -p 80:80 weapp'
            }
        }
    }
}