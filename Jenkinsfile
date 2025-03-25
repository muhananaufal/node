pipeline {
    agent any

    tools {
        nodejs 'NodeJS 23.10.0' // Sesuaikan dengan nama Node.js yang dikonfigurasi di Jenkins
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/muhananaufal/node.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Run Tests') {
            steps {
                echo 'Test successfully...'
            }
        }

        stage('Build') {
            steps {
                sh 'npm run build' // Sesuaikan dengan perintah build di proyek Anda
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying to production environment...'
                // Tambahkan perintah deploy sesuai kebutuhan Anda
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
