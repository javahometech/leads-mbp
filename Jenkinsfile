pipeline{
    agent any

    stages{
        stage("Code Checkout"){
            when {
                branch "develop"
            }
            steps{
                git url:"https://github.com/javahometech/leads-mbp", branch: "main"
            }
        }

        stage("Maven Build"){
            when {
                branch "develop"
            }
            steps{
                sh "mvn clean pacakge"
            }
        }
        stage("Dev Deploy"){
            when {
                branch "develop"
            }
            steps{
                echo "Deploy to development environment"
            }
        }
        stage("Test Deploy"){
            when {
                branch "test"
            }
            steps{
                echo "Deploy to test environment"
            }
        }

        stage("Prod Deploy"){
            when {
                branch "main"
            }
            steps{
                echo "Deploy to prod environment"
            }
        }
        
    }
}