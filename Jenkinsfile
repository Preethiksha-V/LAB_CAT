pipeline {
    agent any

    parameters {
        string(name: 'USERNAME', defaultValue: 'DefaultUser', description: 'Enter your username')
    }

    stages {
        stage('Checkout Latest Version') {
            steps {
                // Checkout latest version from GitHub
                checkout scm
            }
        }

        stage('Create user.txt') {
            steps {
                // Create user.txt and store the username inside it
                bat "echo ${params.USERNAME} > user.txt"
            }
        }

        stage('Verify user.txt') {
            steps {
                // Display the contents of user.txt in Jenkins console
                bat 'type user.txt'
            }
        }
    }
}
