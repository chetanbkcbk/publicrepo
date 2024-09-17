pipeline{
    agent any
    
    stages{
        stage('clone'){
            steps{
                git 'https://github.com/chetanbkcbk/publicrepo.git'
            }
        }
        stage('clean'){
            steps{
                sh 'rm -rf /var/www/html/*'
            }
        }
        stage('deploy'){
            steps{
                sh 'cp -r . /var/www/html/'
            }
        }
    }
}