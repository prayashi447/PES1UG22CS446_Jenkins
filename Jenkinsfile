pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                script {
                    sh 'git clone https://github.com/prayashi447/PES1UG22CS446_Jenkins.git'
                    sh 'cd PES1UG22CS446_Jenkins'
                }
            }
        }

        stage('Build') {
            steps {
                script {
                    sh 'g++ -o PES1UG22CS446-1 PES1UG22CS446_Jenkins/hello.cpp'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './PES1UG22CS446-1'
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    sh 'cd PES1UG22CS446_Jenkins && git add hello.cpp && git commit -m "Added working C++ file" && git push'
                }
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
