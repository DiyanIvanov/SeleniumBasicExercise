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
        parallel{
            stage("Test App 1"){
                steps{
                    bat 'dotnet test TestProject1/TestProject1.csproj --no-build --verbosity normal'
                }
            }
            stage("Test App 2"){
                steps{
                    bat 'dotnet test TestProject2/TestProject2.csproj --no-build --verbosity normal'
                }
            }
            stage("Test App 3"){
                steps{
                    bat 'dotnet test TestProject3/TestProject3.csproj --no-build --verbosity normal'
                }
            }
        }
    }
}