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

        stage("Style"){
            steps{
                echo "Checking Style"
                sh 'npm run eslint'
            }
        }

        stage("Test"){
            steps{
                echo "Testing"
                sh 'npm test'
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