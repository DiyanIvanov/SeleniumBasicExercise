pipeline{
    agent any
    stages{
        stage("Restore Dependancies"){
            steps{
                bat 'dotnet restore'
            }
        }
        stage("Build App"){
            steps{
                bat 'dotnet build --no-restore'
            }
        }
        stage("Test App"){
            steps{
                bat 'dotnet test --no-build --verbosity normal'
            }
        }
    }
}