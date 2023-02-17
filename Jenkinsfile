pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o program_exec test.cpp'
            }
        }
        stage('Test') {
            steps {
                sh './program_exec'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Congrats! Deployment is successful!'
            }
        }
    }

    post {
        
        failure {
            echo 'Sorry! Pipeline has failed.'
        }
    }
}
