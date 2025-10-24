pipeline {
    agent any

    tools {
        // Use the default JDK and Maven installed in Jenkins
        jdk 'JDK11'
        maven 'Maven3'
    }

    parameters {
        string(name: 'BRANCH_NAME', defaultValue: 'main')
        string(name: 'BUILD_ENV', defaultValue: 'dev')
        string(name: 'STUDENT_NAME', defaultValue: 'Muhammad Abdullah Javed')
    }

    environment {
        APP_VERSION = "1.0.0"
    }

    stages {
        stage('Build') {
            steps {
                echo "Building Calculator App v${APP_VERSION}"
                bat "mvn clean compile"
            }
        }

        stage('Test') {
            steps {
                echo "Running unit tests..."
                bat "mvn test"
            }
        }

        stage('Deploy') {
            steps {
                echo "Simulating deployment of Java Calculator App..."
            }
        }
    }

    post {
        success {
            echo "Pipeline executed successfully."
        }
        failure {
            echo "Pipeline failed."
        }
    }
}
