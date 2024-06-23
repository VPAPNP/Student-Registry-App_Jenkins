pipeline
{
    agent any
    stages
    {
        stage('NPM Install')
        {
            steps
            {
                bat 'npm install'
            }
        }
        stage('NPM Audit')
        {
            steps
            {
                bat 'npm audit'
            }
        }
        stage('NPM Integration Test')
        {
            steps
            {
                bat 'npm run test'
            }
        }
    }
}