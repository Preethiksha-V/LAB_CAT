pipeline {
    agent any

    parameters {
        string(name: 'MESSAGE', defaultValue: 'Hello Jenkins', description: 'Message to print')
    }

    stages {
        stage('Checkout Latest Commit') {
            steps {
                // Checkout latest commit from GitHub
                checkout scm
            }
        }

        stage('Create output.txt') {
            steps {
                // Create a file named output.txt using BAT command
                bat 'echo This is output from Jenkins > output.txt'
            }
        }

        stage('Display output.txt Contents') {
            steps {
                // Display the contents of output.txt in Jenkins console
                bat 'type output.txt'
            }
        }

        stage('Print Parameter Again') {
            steps {
                echo "Parameter value is still: ${params.MESSAGE}"
            }
        }
    }
}
