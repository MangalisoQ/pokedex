pipeline {
    agent any

    stages {
        stage("Build"){
            steps{
                echo 'Building...'
                npm install
            }
        }

        stage("Test"){
            steps{
                echo "Testing"
                npm test
                npm run eslint
            }
        }

        stage("Deploy"){
            steps{
                echo "Deploying"
                npm run start-prod
            }
        }

    }
}