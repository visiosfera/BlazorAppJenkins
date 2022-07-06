pipeline {
    agent any

    stages {
        stage ("inicial") {
            steps {
                echo 'Iniciando a pipeline'
            }
        }
        stage('Restore packages'){
           steps{
               sh 'dotnet restore BlazorAppJenkins.sln'
            }
         }
         stage('Clean'){
           steps{
               sh 'dotnet clean BlazorAppJenkins.sln --configuration Release'
            }
         }
        stage('Build'){
           steps{
               sh 'dotnet build BlazorAppJenkins.sln --configuration Release --no-restore'
            }
         }
        stage('Publish'){
             steps{
               sh 'dotnet publish BlazorAppJenkins/BlazorAppJenkins.csproj --configuration Release --no-restore -o /var/www/gerenciadorradioweb'
             }
        }
    }
}