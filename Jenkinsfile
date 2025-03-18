pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the CC lab 8...'
                sh 'make -C main'

            }
        }
        stage('Test') {
            steps {
                echo 'Running the compiled program...'
                sh './main/hello_exec' // Run the executable
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploy step (PES1UG22CS446)'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed. Please check the errors.'
        }
    }
}
