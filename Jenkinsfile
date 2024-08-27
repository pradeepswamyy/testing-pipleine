pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from the branch that triggered the build
                checkout scm
            }
        }

        stage('Build') {
            steps {
                // Example build step (replace with your actual build command)
                echo 'Building the project...'
                // sh './build-script.sh'  // Uncomment and replace with your build command
            }
        }

        stage('Test') {
            steps {
                // Example test step (replace with your actual test command)
                echo 'Running tests...'
                // sh './test-script.sh'  // Uncomment and replace with your test command
            }
        }
    }

    post {
        always {
            // Actions that are always performed, regardless of success or failure
            echo 'Cleaning up...'
            // sh './cleanup-script.sh'  // Uncomment if you have a cleanup step
        }
        success {
            // Actions to perform on successful completion
            echo 'Build and tests were successful!'
        }
        failure {
            // Actions to perform if the build or tests fail
            echo 'Build or tests failed.'
        }
    }
}
