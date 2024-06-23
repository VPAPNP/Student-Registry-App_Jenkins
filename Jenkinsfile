pipeline {
    agent any
    stages {
        stage('NPM Install') {
            steps {
                bat 'npm install'
            }
        }
        stage('NPM Audit') {
            steps {
                bat 'npm audit'
            }
        }
        stage('NPM Integration Test') {
            steps {
                bat 'npm run test'
            }
        }
        stage('Deploy') {
            steps {
                script {
                    def userInput = input(id: 'Deploy', message: 'Deploy to production?', parameters: [choice(name: 'Approve', choices: 'Yes\nNo', description: 'Approve deployment?')])
                    if (userInput == 'No') {
                        error 'Deployment aborted by user'
                    }
                    // Replace 'deploy_command_here' with your actual deployment command
                    echo 'deploy_command_here'
                }
            }
        }
    }
}
