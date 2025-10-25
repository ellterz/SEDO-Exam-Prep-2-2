    pipeline{
        agent{
            label "node"
        }
        stages{
            stage("Restore .NET Packages"){
                steps{
                    sh 'dotnet restore'
                }

                }
            }
            stage("Build .NET Project"){
                step{
                    sh 'dotnet build --no-restore'
                }
            }
            stage("Run Unit and Integration Tests"){
                step{
                    sh 'dotnet test --no-build --verbosity normal'
                }
            }
        }

    }