pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the source code from your repository
                git 'https://github.com/Ayush758/NodeJS-DevOps-Pipeline.git'
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

    post {
        always {
            // Cleanup actions
            cleanWs()
        }
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed.'
        }
    }
}
