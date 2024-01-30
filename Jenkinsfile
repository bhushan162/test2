pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout code from GitHub repository
                git 'https://github.com/bhushan162/test2.git'
            }
        }
        
        stage('Static Analysis') {
            steps {
                // Execute static analysis using SonarQube
                withSonarQubeEnv('SonarQube') {
                    // Assuming you're using a tool like SonarCSS for analyzing CSS code
                    // Adjust the command to run the static analysis tool for CSS
                    sh 'sonar-scanner.bat -D"sonar.projectKey=test_project" -D"sonar.sources=C:/Program Files/Jenkins/workspace/." -D"sonar.host.url=http://localhost:9000" -D"sonar.token=sqp_a04dd056f5277a2227ab4979e06d68b02aa630ae"'sonar.projectBaseDir=C:/Program Files/Jenkins/workspace/
                }
            }
        }

        stage('Build Docker Image') {
            steps {
                // Build Docker image
                script {
                    // Add commands to build Docker image for your CSS project
                    // You may need to copy CSS files to the appropriate directory in the Docker image
                    // Adjust these commands based on your project structure and Docker setup
                }
            }
        }
    }
}
