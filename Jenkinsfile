pipeline {
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
        stage('Sonar Scanner') {
            steps {
                sh 'sonar-scanner'
            }
        }
    }
}
