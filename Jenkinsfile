pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                sh 'echo "--> in build"'
                build 'PES1UG21CS245-1'
                sh 'g++ main.cpp -o output'
            }
        }
        stage('Test') { 
            steps {
            sh 'echo "--> in test"'
                sh './output'

            }
        }
        stage('Deploy') { 
            steps {
                sh 'echo "--> in deployment"' 
                sh 'echo "--> deployed"'
            }
        }
    }
    post{
        failure{
            error '--> pipeline failed'
        }
    }
}
