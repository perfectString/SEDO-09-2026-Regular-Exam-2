pipeline{
    agent any
    stages{
        stage("Restore dependencies"){
            when{
                    branch "main"
            }
            steps{
                bat "dotnet restore" 
            }
            
        }
         stage("Build"){
            when{

                    branch "main" 
            }
            steps{
                bat "dotnet build --no-restore" // this build and restores for windows machines
            }
            
        }
            stage("Test"){
                when{
                        branch "main" 
                }
                steps{
                    bat "dotnet test --no-build --verbosity normal" 
                }
                
            }
    }
}