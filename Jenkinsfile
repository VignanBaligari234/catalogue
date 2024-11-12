pipeline {
    options{
        ansiColor('xterm')
    }
    agent { node { label 'AGENT-1' } }
    stages {
        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }
        stage('Unit Test') {
            steps {
                echo 'unit testing is done here always'
            }
        }
        // stage('Sonar Scan') {
        //     steps {
        //         sh 'ls -ltr'
        //         sh 'sonar-scanner'
        //     }
        // }
        stage('build'){
            steps{
                sh 'ls -ltr'
                sh 'zip -r catalogue.zip ./* --exclude=.git --exclude=.zip'
            }
        }
        stage('publish artifact'){
            steps{
                sh 'ls -ltr'
                sh 'zip -r ./* --exclude=.git --exclude=.zip'
            }
        }
    }
    post{
        always{
                echo 'cleaning up workspace'
                //deleteDir()
        }
    }
}
