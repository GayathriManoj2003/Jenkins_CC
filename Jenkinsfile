pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                build 'PES1UG21CS904-1'
                sh 'g++ main.cpp -o output_file'
            }
        }

        stage('Test') {
            steps {
                sh './output_file'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploy stage'
            }
        }
    }

    post {
        failure {
            error 'Pipeline failed'
        }
    }
}
