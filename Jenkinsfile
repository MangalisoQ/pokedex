pipeline {
    agent any

    tools {
        nodejs '16.20.2'
    }

    stages {
        stage("Build"){
            steps{
                echo 'Building...'
                sh 'npm install'
            }
        }

        stage("Test"){
            steps{
                echo "Testing"
                sh 'npm test'
                sh 'npm run eslint'
            }
        }

        stage("Deploy"){
            steps{
                echo "Deploying"
                sh 'npm run start-prod'
            }
        }

    }
}