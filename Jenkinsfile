pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o PES1UG22C712-1 main.cpp'  // Compile the C++ file
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './PES1UG22CS712-1'  // Execute the compiled file
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
            }
        }
    }

    post {
        success {
            echo 'Pipeline executed successfully!'
        }
        failure {
            echo 'Pipeline failed'
        }
    }
}
