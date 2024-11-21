pipeline {
    agent any

    environment {
        // Define any global environment variables here
        PATH = "${env.PATH};C:\\Program Files\\Git\\bin" // Add Git to the PATH if needed
    }

    stages {
        stage('Checkout Code') {
            steps {
                echo 'Checking out code from Git repository...'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building the project...'
                bat 'echo Build step executed' // Replace with your build command (e.g., `mvn clean install`)
            }
        }

        stage('Run Tests') {
            steps {
                echo 'Running tests...'
                bat 'echo Test step executed' // Replace with your test command (e.g., `mvn test`)
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the project...'
                bat 'echo Deployment step executed' // Replace with your deploy command
            }
        }
    }

    post {
        always {
            echo 'Cleaning up workspace...'
            cleanWs()
        }

        success {
            echo 'Pipeline completed successfully!'
        }

        failure {
            echo 'Pipeline failed. Please check logs for details.'
        }
    }
}
