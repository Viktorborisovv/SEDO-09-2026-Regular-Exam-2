pipeline {
    agent any

    stages {
        stage('Restore dependencies') {
            steps {
                bat 'dotnet restore Homies.sln'
            }
        }

        stage('Build the project') {
            steps {
                bat 'dotnet build Homies.sln --no-restore'
            }
        }

        stage('Run tests') {
            steps {
                bat 'dotnet test Homies.sln --no-build --verbosity normal'
            }
        }
    }
}