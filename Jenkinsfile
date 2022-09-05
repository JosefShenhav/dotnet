pipeline {
    agent any

    stages {
        stage('Build') {
            steps {       
                def scannerHome = tool 'SonarScanner for MSBuild'
                withSonarQubeEnv() {
                  sh "dotnet ${scannerHome}/SonarScanner.MSBuild.dll begin /k:\"lord\""
                  sh "dotnet build"
                  sh "dotnet ${scannerHome}/SonarScanner.MSBuild.dll end"
                }
            }
        }
    }
}
