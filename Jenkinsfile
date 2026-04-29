pipeline {
    agent any

    environment {
        GIT_REPO = 'https://github.com/pratikshaba/practice.git'
        BRANCH = 'main'
    }

    stages {

        stage('Checkout') {
            steps {
                echo "Cloning repository..."
                git branch: "${BRANCH}", url: "${GIT_REPO}"
            }
        }

        stage('Verify Environment') {
            steps {
                echo "Checking system tools..."
                sh 'java -version'
                sh 'git --version'
            }
        }

        stage('Build') {
            steps {
                echo "Build stage running..."
                sh 'echo "Replace this with Maven/Gradle build command"'
            }
        }

        stage('Test') {
            steps {
                echo "Test stage running..."
                sh 'echo "Add unit test commands here"'
            }
        }

        stage('Package') {
            steps {
                echo "Packaging application..."
                sh 'echo "Add packaging step (jar/war/docker)"'
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploy stage running..."
                sh 'echo "Add deployment script here"'
            }
        }
    }

    post {
        success {
            echo "Pipeline SUCCESS 🎉"
        }
        failure {
            echo "Pipeline FAILED ❌"
        }
        always {
            echo "Pipeline finished."
        }
    }
}
