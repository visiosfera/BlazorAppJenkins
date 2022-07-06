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
    }
}