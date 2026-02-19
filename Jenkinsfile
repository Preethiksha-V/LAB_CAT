pipeline {
    agent any

    parameters {
        string(name: 'MESSAGE', defaultValue: 'Hello Jenkins', description: 'Message to print')
    }

    stages {
        stage('Checkout Updated Code') {
            steps {
                // Checkout updated source code from GitHub
                checkout scm
            }
        }

        stage('Display System Date') {
            steps {
                // Windows BAT command to show current system date
                bat 'echo Current System Date: %date%'
            }
        }

        stage('Print Parameter Again') {
            steps {
                echo "Verifying parameter value again: ${params.MESSAGE}"
            }
        }
    }
}
