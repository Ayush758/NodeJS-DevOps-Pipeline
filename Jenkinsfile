pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the source code from your repository
                git 'https://github.com/Mahmoud-Sh3ban/NodeJS-DevOps-Pipeline.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                script {
                    // Install Node.js dependencies
                    sh 'npm install --omit=dev && npm install express'
                }
            }
        }

        stage('Run Application') {
            steps {
                script {
                    // Run the application
                    sh 'node app.js'
                }
            }
        }
    }
